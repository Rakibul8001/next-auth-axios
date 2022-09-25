# What is this?
JWT authentication with axios in nextjs.

# Installation
`npm i mri-axios --save`

# Usage

```
import MRIAxios form 'mri-axios'

const {http} = MRIAxios();

  async function submitForm(e) {
    e.preventDefault();

    let body={...employee, action:"addEmployee"}

      await http.post(`${process.env.NEXT_PUBLIC_DOMAIN}/app/hrm/employee`, body)
      .then((res)=>{
          console.log(res.data.data)

      }).catch((err)=>{
        console.log(err)
      });

  }

```
