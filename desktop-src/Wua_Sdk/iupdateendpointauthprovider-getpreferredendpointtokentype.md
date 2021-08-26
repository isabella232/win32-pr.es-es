---
description: Devuelve el tipo preferido de token de autenticación para el punto de conexión del servicio.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: Método IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a9b7d15d6d27170106118c720d25567389884c50e27aac202adedf00290236c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994585"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType (método)

Devuelve el tipo preferido de token de autenticación para el punto de conexión del servicio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*serviceId* \[ En\]
</dt> <dd>

Identifica el servicio que se va a actualizar.

</dd> <dt>

*endpointType* \[ En\]
</dt> <dd>

Identifica el tipo de punto de conexión que se necesita para conectarse al servicio.

</dd> <dt>

*ulRequestedTypes* \[ En\]
</dt> <dd>

Identifica el conjunto de tokens de ORed que admite el punto de conexión.

</dd> <dt>

*pulPreferredTokenTypes* \[ out\]
</dt> <dd>

Especifique el conjunto ORed de tipos de token de autenticación preferidos. (Establezca en 0 para indicar que no se necesita ningún token de autenticación).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente. De lo contrario, devuelve un código de error COM Windows.

## <a name="remarks"></a>Comentarios

Cuando se devuelve este método, WUA elige un tipo de token entre los tipos preferidos y lo pasa al parámetro tokenType del [**método GetEndpointToken.**](iupdateendpointauthprovider-getendpointtoken.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




