---
description: Las variables de tipo variante tienen un campo de etiqueta de tipo VT que indica el tipo de datos de los datos.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Establecer el campo de etiqueta de tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275177"
---
# <a name="setting-the-type-tag-field"></a>Establecer el campo de etiqueta de tipo

Las variables de tipo **variante** tienen un campo de etiqueta de tipo **VT** que indica el tipo de datos de los datos. Los métodos devuelven los valores devueltos de tipo **Variant** con el campo de etiqueta de tipo establecido en el tipo de datos del valor devuelto. Los parámetros de entrada de tipo **Variant** en una llamada al método deben tener el campo de etiqueta de tipo establecido por la aplicación en uno de los valores admitidos. La correspondencia entre los tipos de parámetro y los tipos de datos es la siguiente.



| Tipo de parámetro              | Tipo de datos                                      |
|-----------------------------|------------------------------------------------|
| PROPTYPE \_ largo<br/>   | VT \_ I2 o VT \_ I4<br/>                    |
| fecha de PROPTYPE \_<br/>   | fecha de VT \_<br/>                            |
| \_binario PROPTYPE<br/> | VT \_ BSTR o (VT \_ BSTR \| VT \_ BYREF)<br/> |
| \_cadena PROPTYPE<br/> | VT \_ BSTR o (VT \_ BSTR \| VT \_ BYREF)<br/> |



 

En el ejemplo siguiente se muestra cómo inicializar los tipos de datos Variant enumerados anteriormente.


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




