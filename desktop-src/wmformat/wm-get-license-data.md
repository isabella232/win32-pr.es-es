---
title: WM_GET_LICENSE_DATA estructura (Drmexternals. h)
description: La estructura de datos de la licencia de Get de WM \_ \_ \_ contiene información sobre dónde adquirir una licencia DRM.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- WM_GET_LICENSE_DATA estructura de Windows Media Format
topic_type:
- apiref
api_name:
- WM_GET_LICENSE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f238bea29ab7271896dc7516b6424e4cc298f5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422306"
---
# <a name="wm_get_license_data-structure"></a>\_Estructura de \_ datos de licencia de obtención de WM \_

La estructura de datos de la licencia de Get de WM contiene información sobre dónde adquirir una [*licencia*](wmformat-glossary.md) [*DRM*](wmformat-glossary.md) . **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMGetLicenseData {
  DWORD   dwSize;
  HRESULT hr;
  WCHAR   *wszURL;
  WCHAR   *wszLocalFilename;
  BYTE    *pbPostData;
  DWORD   dwPostDataSize;
} WM_GET_LICENSE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

**DWORD** que contiene el tamaño de la estructura de datos de la **\_ \_ licencia \_ de WM Get** , en bytes.

</dd> <dt>

**h**
</dt> <dd>

Código de retorno **HRESULT** .

</dd> <dt>

**wszURL**
</dt> <dd>

Cadena terminada en NULL de caracteres anchos que contiene la dirección URL de adquisición de licencias. Use esta cadena y la cadena **pbPostData** en la adquisición de licencias no silenciosa.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Cadena terminada en NULL de caracteres anchos que contiene una página HTML local generada por el componente DRM. Cuando esta cadena se carga en un explorador, redirige automáticamente la solicitud HTTP a la dirección URL de adquisición de licencias, junto con los datos post necesarios. El uso de esta dirección URL local ahora está en desuso. El enfoque recomendado es usar las cadenas **wszURL** y **pbPostData** .

</dd> <dt>

**pbPostData**
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos que se van a exponer en la dirección URL de adquisición de licencias. Debe agregar la siguiente cadena al principio de la cadena **pbPostData** : "nonsilent = 1&Challenge =". La cadena resultante se debe anexar a **wszURL** al formar la solicitud HTTP.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**DWORD** que indica el tamaño de **pbPostData** sin la cadena "nonsilent = 1&Challenge =" a la que se hace referencia en **pbPostData**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura rellenada se devuelve en el parámetro *pValue* del método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) si **el \_ Estado de WMT** es igual a **WMT \_ sin \_ derechos \_ ex** o la **\_ \_ licencia de adquisición de WMT**. En el caso de \_ los eventos de WMT no \_ Rights \_ ex, el miembro **HR** será la \_ licencia NS e requerida, la licencia \_ \_ NS \_ e \_ \_ obsoleta o los \_ \_ \_ derechos incorrectos \_ . Cualquiera de estos errores indica que se debe adquirir una nueva licencia navegando a la dirección URL del miembro **wszURL** .

En el caso de los eventos de licencia de adquisición de WMT \_ \_ , el miembro **HR** pasará la macro Succeeded si se adquirió correctamente una licencia. Si este evento se recibe después de un intento de adquisición silenciosa y **HR** es igual a NS \_ E \_ DRM \_ License \_ NOTACQUIRED, indica que el servidor de licencias solo admite la adquisición no silenciosa para esta licencia.

La aplicación de ejemplo AudioPlayer muestra cómo utilizar correctamente la información devuelta en esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | SDK de Windows Media Format 7 o versiones posteriores del SDK<br/>                       |
| Encabezado<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





