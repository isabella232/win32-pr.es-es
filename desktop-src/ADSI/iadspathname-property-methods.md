---
title: Métodos de propiedad IADsPathname (Iads.h)
description: Obtiene o establece las propiedades EscapedMode.
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
ms.openlocfilehash: 11d3321d58065d890d864ed967a4e6a66dad22cde2cc234b5907afab74986898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023433"
---
# <a name="iadspathname-property-methods"></a>Métodos de propiedad IADsPathname

Los métodos de propiedad [**de la interfaz IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) obtienen o establecen las **propiedades EscapedMode.** Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**EscapedMode**
</dt> <dd> <dl>

Examine o especifique cómo se controlan los caracteres de escape en un pathname. Para obtener más información y opciones definidas, vea [**ADS \_ ESCAPE MODE \_ \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **Long**
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

 

## <a name="remarks"></a>Comentarios

**EscapedMode representa** un estado. Puede activarla o desactivarla si la establece en ADS ESCAPEDMODE ON o \_ \_ ADS \_ ESCAPEDMODE \_ OFF/ADS \_ ESCAPEDMODE OFF \_ \_ EX. Cuando está activada o desactivada, todas las recuperaciones posteriores generan cadenas de ruta de acceso con escape o sin escape.

En ADSI, solo [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) es capaz de desencapsular las rutas de acceso. Todas las demás interfaces ADSI siempre devuelven rutas de acceso con escape. El estado predeterminado de **EscapedMode es** ADS \_ ESCAPEDMODE \_ DEFAULT, tal como se define en [**ADS ESCAPE MODE \_ \_ \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar la propiedad **EscapedMode** para activar o desactivar el escape de los tres caracteres especiales siguientes: "=","," y "/".


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



En el ejemplo de código siguiente se muestra cómo usar la propiedad **EscapedMode** para activar o desactivar el escape de los tres caracteres especiales siguientes: "=","," y "/".


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



En el ejemplo de código siguiente se muestra cómo trabajar con la **propiedad EscapedMode.** Se omite la comprobación de errores.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsPathname se define como \_ D592AED4-F420-11D0-A36E-00C04FB950DC<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[**ENUMERACIÓN \_ DEL MODO DE ESCAPE DE \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





