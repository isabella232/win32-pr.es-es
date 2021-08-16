---
title: WM_GET_LICENSE_DATA estructura (Drternals.h)
description: La estructura \_ WM GET LICENSE DATA contiene información sobre dónde adquirir una licencia \_ \_ DRM.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- WM_GET_LICENSE_DATA windows Media Format de estructura
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
ms.openlocfilehash: f5f53b6ddfd532710e712637c57785d8893d8f977807bfb45cac0fc787ccbf58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844480"
---
# <a name="wm_get_license_data-structure"></a>Estructura \_ DE DATOS DE WM GET \_ LICENSE \_

La **estructura WM GET LICENSE \_ \_ \_ DATA** contiene información sobre dónde adquirir una [*licencia DRM.*](wmformat-glossary.md) [](wmformat-glossary.md)

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

**DWORD que** contiene el tamaño de la estructura **WM GET LICENSE \_ \_ \_ DATA,** en bytes.

</dd> <dt>

**h**
</dt> <dd>

**Código de retorno HRESULT.**

</dd> <dt>

**wszURL**
</dt> <dd>

Cadena terminada en null de caracteres anchos que contiene la dirección URL de adquisición de licencias. Use esta cadena y la **cadena pbPostData en** la adquisición de licencias no silenciosas.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Cadena terminada en null de caracteres anchos que contiene una página HTML local generada por el componente DRM. Cuando esta cadena se carga en un explorador, redirige automáticamente la solicitud HTTP a la dirección URL de adquisición de licencia, junto con los datos posteriores necesarios. El uso de esta dirección URL local está ahora en desuso. El enfoque recomendado es usar las **cadenas wszURL** y **pbPostData.**

</dd> <dt>

**pbPostData**
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos que se publicarán en la dirección URL de adquisición de licencias. Debe agregar la siguiente cadena al principio de la cadena **pbPostData:** "nonsilent=1&challenge=". La cadena resultante se debe anexar a **wszURL** al formar la solicitud HTTP.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**DWORD** que indica el tamaño de **pbPostData** sin la cadena "nonsilent=1&challenge=" a la que se hace referencia en **pbPostData**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura rellenada se devuelve en el parámetro *pValue* del método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) si **WMT \_ STATUS** es igual a **WMT \_ NO RIGHTS \_ \_ EX** o **WMT ACQUIRE \_ \_ LICENSE.** Para los eventos WMT NO RIGHTS EX, el miembro hr será \_ \_ \_ NS E LICENSE  \_ \_ \_ REQUIRED, NS E LICENSE OUTOFDATE o \_ \_ \_ NS E LICENSE INCORRECT \_ \_ \_ \_ RIGHTS. Cualquiera de estos errores indica que se debe adquirir una nueva licencia navegando a la dirección URL del **miembro wszURL.**

Para los eventos ACQUIRE LICENSE de WMT, el miembro hr pasará la \_ \_ macro SUCCEEDED si una licencia se adquirió correctamente.  Si este evento se recibe después de  un intento de adquisición silenciosa y hr es igual a NS \_ E DRM LICENSE \_ \_ NOTACQUIRED, indica que el servidor de licencias solo admite la adquisición no silenciosa para esta \_ licencia.

La aplicación de ejemplo Audioplayer muestra cómo usar correctamente la información devuelta en esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 7 o versiones posteriores del SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drternals.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





