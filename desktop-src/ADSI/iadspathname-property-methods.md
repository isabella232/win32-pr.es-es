---
title: Métodos de la propiedad IADsPathname (iAds. h)
description: Obtiene o establece las propiedades de EscapedMode.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPathname ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274534"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="699dc-104">Métodos de propiedad IADsPathname</span><span class="sxs-lookup"><span data-stu-id="699dc-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="699dc-105">Los métodos de propiedad de la interfaz [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) obtienen o establecen las propiedades **EscapedMode** .</span><span class="sxs-lookup"><span data-stu-id="699dc-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="699dc-106">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="699dc-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="699dc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="699dc-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="699dc-108">**EscapedMode**</span><span class="sxs-lookup"><span data-stu-id="699dc-108">**EscapedMode**</span></span>
<span data-ttu-id="699dc-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="699dc-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="699dc-110">Examine o especifique cómo se controlan los caracteres de escape en un nombreruta.</span><span class="sxs-lookup"><span data-stu-id="699dc-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="699dc-111">Para obtener más información y opciones definidas, [**consulte \_ \_ \_ enumeración de modo de escape de ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="699dc-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="699dc-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="699dc-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="699dc-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="699dc-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="699dc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="699dc-114">Remarks</span></span>

<span data-ttu-id="699dc-115">**EscapedMode** representa un estado.</span><span class="sxs-lookup"><span data-stu-id="699dc-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="699dc-116">Puede activarlo o desactivarlo, estableciéndolo en ADS \_ ESCAPEDMODE \_ on o ADS \_ ESCAPEDMODE \_ OFF/ADS \_ ESCAPEDMODE \_ OFF \_ .</span><span class="sxs-lookup"><span data-stu-id="699dc-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="699dc-117">Cuando está activada o desactivada, todas las recuperaciones posteriores producen cadenas de ruta de acceso con escape o sin escape.</span><span class="sxs-lookup"><span data-stu-id="699dc-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="699dc-118">En ADSI solo el [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) es capaz de desescapar rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="699dc-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="699dc-119">Todas las demás interfaces ADSI siempre devuelven rutas de acceso con escape.</span><span class="sxs-lookup"><span data-stu-id="699dc-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="699dc-120">El estado predeterminado de **EscapedMode** es ADS \_ EscapedMode \_ default, tal y como se define en la [**\_ \_ \_ enumeración de modo de escape de ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="699dc-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="699dc-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="699dc-121">Examples</span></span>

<span data-ttu-id="699dc-122">En el ejemplo de código siguiente se muestra cómo usar la propiedad **EscapedMode** para activar o desactivar el escape de los tres caracteres especiales siguientes: "=", "," y "/".</span><span class="sxs-lookup"><span data-stu-id="699dc-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="699dc-123">En el ejemplo de código siguiente se muestra cómo usar la propiedad **EscapedMode** para activar o desactivar el escape de los tres caracteres especiales siguientes: "=", "," y "/".</span><span class="sxs-lookup"><span data-stu-id="699dc-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="699dc-124">En el ejemplo de código siguiente se muestra cómo trabajar con la propiedad **EscapedMode** .</span><span class="sxs-lookup"><span data-stu-id="699dc-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="699dc-125">Se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="699dc-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="699dc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="699dc-126">Requirements</span></span>



| <span data-ttu-id="699dc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="699dc-127">Requirement</span></span> | <span data-ttu-id="699dc-128">Value</span><span class="sxs-lookup"><span data-stu-id="699dc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="699dc-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="699dc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="699dc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="699dc-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="699dc-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="699dc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="699dc-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="699dc-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="699dc-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="699dc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="699dc-134"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="699dc-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="699dc-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="699dc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="699dc-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="699dc-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="699dc-137">IID</span><span class="sxs-lookup"><span data-stu-id="699dc-137">IID</span></span><br/>                      | <span data-ttu-id="699dc-138">IID \_ IADsPathname se define como D592AED4-F420-11D0-A36E-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="699dc-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="699dc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="699dc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="699dc-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="699dc-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="699dc-141">**\_ \_ enumeración de modo de escape de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="699dc-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





