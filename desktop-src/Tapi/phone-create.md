---
description: El mensaje TAPI PHONE \_ CREATE se envía para informar a las aplicaciones de la creación de un nuevo dispositivo telefónico.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: PHONE_CREATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071099"
---
# <a name="phone_create-message"></a>Mensaje \_ PHONE CREATE

El mensaje **TAPI PHONE \_ CREATE** se envía para informar a las aplicaciones de la creación de un nuevo dispositivo telefónico.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam1* 
</dt> <dd>

*HDeviceID del* dispositivo recién creado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las aplicaciones que negociaron la versión 1.3 de la API se envían un mensaje [**PHONE \_ STATE**](phone-state.md) que especifica PHONESTATE REINIT, que les exige que apaguen su uso de la API y llamen a \_ [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) de nuevo para obtener el nuevo número de dispositivos. Sin embargo, tapi versión 1.4 y posteriores no requieren que todas las aplicaciones se apaguen antes de permitir que las aplicaciones se reinicialicen; La reinicialización puede tener lugar inmediatamente cuando se crea un nuevo dispositivo.

Las aplicaciones que admiten TAPI versión 1.4 o posterior se envían un **mensaje PHONE \_ CREATE.** Esto les informa de la existencia del nuevo dispositivo y su nuevo identificador de dispositivo. A continuación, la aplicación puede elegir si intenta o no trabajar con el nuevo dispositivo en su momento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ESTADO DEL \_ TELÉFONO**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




