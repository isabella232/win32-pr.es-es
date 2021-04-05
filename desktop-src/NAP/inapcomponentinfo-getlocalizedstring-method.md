---
title: Método INapComponentInfo GetLocalizedString (NapCommon. h)
description: Lo usa el sistema NAP para obtener cadenas traducidas.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Método GetLocalizedString NAP
- Método GetLocalizedString NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997156"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>INapComponentInfo:: GetLocalizedString (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetLocalizedString** para obtener cadenas localizadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*msgId* \[ de\]
</dt> <dd>

[**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la cadena que se va a localizar.

</dd> <dt>

*cadena* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión localizada del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Las cadenas deben localizarse según el identificador de idioma del subproceso que realiza la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





