---
description: El \_ mensaje de creación del teléfono TAPI se envía para informar a las aplicaciones de la creación de un nuevo dispositivo telefónico.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Mensaje de PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679060"
---
# <a name="phone_create-message"></a>Mensaje de creación de teléfono \_

El mensaje **de \_ creación del teléfono** TAPI se envía para informar a las aplicaciones de la creación de un nuevo dispositivo telefónico.


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

A las aplicaciones que negociaron la versión de API 1,3 se les envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) que especifica PHONESTATE \_ reinit, que les obliga a apagar su uso de la API y llama a [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) de nuevo para obtener el nuevo número de dispositivos. Sin embargo, la versión 1,4 y posteriores de TAPI no requieren que se cierren todas las aplicaciones antes de permitir que las aplicaciones se reinicialicen. la reinicialización puede realizarse inmediatamente cuando se crea un nuevo dispositivo.

Las aplicaciones que admiten la versión 1,4 o posterior de TAPI recibirán un mensaje de **\_ creación de teléfono** . Esto informa de la existencia del nuevo dispositivo y su nuevo identificador de dispositivo. A continuación, la aplicación puede elegir si desea o no intentar trabajar con el nuevo dispositivo en su momento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estado del teléfono \_**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




