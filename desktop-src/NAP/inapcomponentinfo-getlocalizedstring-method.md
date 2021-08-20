---
title: Método INapComponentInfo GetLocalizedString (NapCommon.h)
description: El sistema NAP lo usa para obtener cadenas localizadas.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Método NAP getLocalizedString
- Método NAP de GetLocalizedString, interfaz INapComponentInfo
- INapComponentInfo interface NAP , GetLocalizedString method
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
ms.openlocfilehash: e7be55595bf6c5af6e435d9c53c9b473a721005699da494319ba55eaa828da2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134368"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>INapComponentInfo::GetLocalizedString (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo::GetLocalizedString** para obtener cadenas localizadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*msgId* \[ En\]
</dt> <dd>

MessageId [**que**](nap-datatypes.md) contiene el identificador de recurso de la cadena que se debe encontrar.

</dd> <dt>

*cadena* \[ out\]
</dt> <dd>

Puntero a un puntero a [**countedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión localizada del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Las cadenas deben localizarse según el identificador de idioma del subproceso que realiza la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





