---
description: '\_Se envía el mensaje de creación de línea TAPI para informar a la aplicación de la creación de un nuevo dispositivo de línea.'
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Mensaje de LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690414"
---
# <a name="line_create-message"></a>Mensaje de creación de línea \_

Se envía el mensaje de **\_ creación de línea** TAPI para informar a la aplicación de la creación de un nuevo dispositivo de línea.


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

*HDeviceID* del dispositivo recién creado.

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

Las aplicaciones anteriores (que negoció la versión 1,3 de TAPI) se envían a un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que especifica LINEDEVSTATE \_ reinit, que les obliga a apagar el uso de la API y a llamar a [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) de nuevo para obtener el nuevo número de dispositivos. Sin embargo, a diferencia de las versiones anteriores de TAPI, esta versión no requiere que se cierren todas las aplicaciones antes de permitir que las aplicaciones se reinicialicen. la reinicialización puede tener lugar inmediatamente cuando se crea un nuevo dispositivo (el cierre completo sigue siendo necesario cuando se quita un proveedor de servicios del sistema).

Las aplicaciones que admiten la versión 1,4 o posterior de TAPI se envían al mensaje de **\_ creación de línea** . Esto informa de la existencia del nuevo dispositivo y su nuevo identificador de dispositivo. A continuación, la aplicación puede elegir si desea o no intentar trabajar con el nuevo dispositivo en su momento. Este mensaje se envía a todas las aplicaciones que admiten esta versión o versiones posteriores de la API que han llamado a [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluidos los que no tienen dispositivos de línea abiertos en este momento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




