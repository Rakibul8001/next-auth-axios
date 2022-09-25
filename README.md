# What is this?

JWT authentication with axios in nextjs.

# Installation

npm i @mdrakibul8001/axios

# Usage

```
import MRIAxios from '@mdrakibul8001/axios';

const {http} = MRIAxios();

  async function submitForm(e) {
    e.preventDefault();

    let body={...employee, action:"addEmployee"}

      await http.post(`URL`, body)
      .then((res)=>{
          console.log(res.data.data)

      }).catch((err)=>{
        console.log(err)
      });

  }

```

# Create Token

```
  const {http,saveToken,user} = MRIAxios();

  http.post(`URL`,{email:email, password:password}).then((res)=>{
    saveToken(res.data.data, res.data.response);
  })

```

# Options

```
const {http,saveToken,getToken,user,token,logout} = MRIAxios();

```
