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
# <a name="setting-the-type-tag-field"></a><span data-ttu-id="39470-103">Establecer el campo de etiqueta de tipo</span><span class="sxs-lookup"><span data-stu-id="39470-103">Setting the Type Tag Field</span></span>

<span data-ttu-id="39470-104">Las variables de tipo **variante** tienen un campo de etiqueta de tipo **VT** que indica el tipo de datos de los datos.</span><span class="sxs-lookup"><span data-stu-id="39470-104">**VARIANT** type variables have a type tag field **vt** that indicates the data type of the data.</span></span> <span data-ttu-id="39470-105">Los métodos devuelven los valores devueltos de tipo **Variant** con el campo de etiqueta de tipo establecido en el tipo de datos del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="39470-105">**VARIANT** type return values are returned by methods with the type tag field set to the data type of the return value.</span></span> <span data-ttu-id="39470-106">Los parámetros de entrada de tipo **Variant** en una llamada al método deben tener el campo de etiqueta de tipo establecido por la aplicación en uno de los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="39470-106">**VARIANT** type input parameters in a method call must have the type tag field set by the application to one of the supported values.</span></span> <span data-ttu-id="39470-107">La correspondencia entre los tipos de parámetro y los tipos de datos es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="39470-107">The correspondence of parameter types to data types is as follows.</span></span>



| <span data-ttu-id="39470-108">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="39470-108">Parameter type</span></span>              | <span data-ttu-id="39470-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="39470-109">Data type</span></span>                                      |
|-----------------------------|------------------------------------------------|
| <span data-ttu-id="39470-110">PROPTYPE \_ largo</span><span class="sxs-lookup"><span data-stu-id="39470-110">PROPTYPE\_LONG</span></span><br/>   | <span data-ttu-id="39470-111">VT \_ I2 o VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="39470-111">VT\_I2 or VT\_I4</span></span><br/>                    |
| <span data-ttu-id="39470-112">fecha de PROPTYPE \_</span><span class="sxs-lookup"><span data-stu-id="39470-112">PROPTYPE\_DATE</span></span><br/>   | <span data-ttu-id="39470-113">fecha de VT \_</span><span class="sxs-lookup"><span data-stu-id="39470-113">VT\_DATE</span></span><br/>                            |
| <span data-ttu-id="39470-114">\_binario PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="39470-114">PROPTYPE\_BINARY</span></span><br/> | <span data-ttu-id="39470-115">VT \_ BSTR o (VT \_ BSTR \| VT \_ BYREF)</span><span class="sxs-lookup"><span data-stu-id="39470-115">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |
| <span data-ttu-id="39470-116">\_cadena PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="39470-116">PROPTYPE\_STRING</span></span><br/> | <span data-ttu-id="39470-117">VT \_ BSTR o (VT \_ BSTR \| VT \_ BYREF)</span><span class="sxs-lookup"><span data-stu-id="39470-117">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |



 

<span data-ttu-id="39470-118">En el ejemplo siguiente se muestra cómo inicializar los tipos de datos Variant enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="39470-118">The following example shows how to initialize the variant data types listed above.</span></span>


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



 

 




