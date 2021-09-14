---
description: El mensaje TAPI LINE \_ CREATE se envía para informar a la aplicación de la creación de un nuevo dispositivo de línea.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: LINE_CREATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250167"
---
# <a name="line_create-message"></a>Mensaje \_ LINE CREATE

El mensaje TAPI **LINE \_ CREATE** se envía para informar a la aplicación de la creación de un nuevo dispositivo de línea.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam1* 
</dt> <dd>

*hDeviceID del* dispositivo recién creado.

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

Las aplicaciones anteriores (que negociaron la versión 1.3 de TAPI) se envían un mensaje [**\_ LINE LINEDEVSTATE**](line-linedevstate.md) que especifica LINEDEVSTATE REINIT, que requiere que apaguen su uso de la API y llamen a \_ [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) de nuevo para obtener el nuevo número de dispositivos. Sin embargo, a diferencia de las versiones anteriores de TAPI, esta versión no requiere que todas las aplicaciones se apaguen antes de permitir que las aplicaciones se reinicialicen. La reinicialización puede tener lugar inmediatamente cuando se crea un nuevo dispositivo (todavía se requiere el apagado completo cuando se quita un proveedor de servicios del sistema).

Las aplicaciones que admiten TAPI versión 1.4 o posterior se envían un **mensaje LINE \_ CREATE.** Esto les informa de la existencia del nuevo dispositivo y su nuevo identificador de dispositivo. A continuación, la aplicación puede elegir si intenta o no trabajar con el nuevo dispositivo en su momento. Este mensaje se envía a todas las aplicaciones que admiten esta o versiones posteriores de la API que han llamado [**a lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx,**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)incluidas aquellas que no tienen ningún dispositivo de línea abierto en ese momento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




