---
description: Devuelve el tipo de token de autenticación preferido para el extremo del servicio.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (método) (UpdateEndpointAuth. h)'
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
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275539"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (método)

Devuelve el tipo de token de autenticación preferido para el extremo del servicio.

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

*serviceId* \[ de\]
</dt> <dd>

Identifica el servicio que se va a actualizar.

</dd> <dt>

*endpointType* \[ de\]
</dt> <dd>

Identifica el tipo de punto de conexión tneeded para conectarse al servicio.

</dd> <dt>

*ulRequestedTypes* \[ de\]
</dt> <dd>

Identifica el conjunto de tokens ORed que admite el extremo.

</dd> <dt>

*pulPreferredTokenTypes* \[ enuncia\]
</dt> <dd>

Especifique el conjunto ORed de tipos de token de autenticación preferidos. (Se establece en 0 para indicar que no se necesita ningún token de autenticación).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente. De lo contrario, devuelve un código de error COM o Windows.

## <a name="remarks"></a>Observaciones

Cuando se devuelve este método, WUA elige un tipo de token de los tipos preferidos y lo pasa al parámetro tokenType del método [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>                |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




