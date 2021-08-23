---
description: El mensaje TAPI LINE \_ LINEDEVSTATE se envía cuando el estado de un dispositivo de línea ha cambiado. La aplicación puede invocar lineGetLineDevStatus para determinar el nuevo estado de la línea.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: LINE_LINEDEVSTATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261e7527354b84801437e48ffc13ba4dbad60ced0cca61be65eb96ce6417bb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682395"
---
# <a name="line_linedevstate-message"></a>Mensaje \_ LINE LINEDEVSTATE

El mensaje TAPI **LINE \_ LINEDEVSTATE** se envía cuando el estado de un dispositivo de línea ha cambiado. La aplicación puede invocar [**lineGetLineDevStatus para**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) determinar el nuevo estado de la línea.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del dispositivo de línea. Este parámetro es **NULL cuando** *dwParam1* es LINEDEVSTATE \_ REINIT.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea. Si el *parámetro dwParam1* es LINEDEVSTATE \_ REINIT, el parámetro *dwCallbackInstance* no es válido y se establece en cero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Elemento de estado del dispositivo de línea que ha cambiado. El parámetro puede ser una o varias de las [**constantes LINEDEVSTATE \_**](linedevstate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

La interpretación de este parámetro depende del valor de *dwParam1*. Si *dwParam1* es LINEDEVSTATE \_ RINGING, *dwParam2* contiene el modo de anillo con el que el conmutador indica a la línea que se debe llamar. Los modos de anillo válidos son números del intervalo uno a **dwNumRingModes,** donde **dwNumRingModes** es una funcionalidad de dispositivo de línea.

Si *dwParam1* es LINEDEVSTATE REINIT y TAPI emitió el mensaje como resultado de la traducción de un nuevo mensaje de API en un mensaje \_ REINIT, *dwParam2* contiene el parámetro *dwMsg* del mensaje original (por ejemplo, [**LINE \_ CREATE**](line-create.md) o LINE \_ LINEDEVSTATE). Si *dwParam2* es cero, esto indica que el mensaje REINIT es un mensaje REINIT "real" que requiere que la aplicación llame a [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) lo antes posible.

</dd> <dt>

*dwParam3* 
</dt> <dd>

La interpretación de este parámetro depende del valor de *dwParam1*. Si *dwParam1* es LINEDEVSTATE \_ RINGING, *dwParam3* contiene el número de anillos para este evento de anillo. El recuento de anillos comienza en cero.

Si *dwParam1* es LINEDEVSTATE REINIT y TAPI emitió el mensaje como resultado de la traducción de un nuevo mensaje de API en un mensaje REINIT, dwParam3 contiene el parámetro \_ *dwParam1* del mensaje original (por ejemplo, LINEDEVSTATE TRANSLATECHANGE o algún otro valor LINEDEVSTATE, si  dwParam2 es LINE LINEDEVSTATE o el nuevo identificador de \_ \_  \_ dispositivo, si *dwParam2* es LINE [**\_ CREATE).**](line-create.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El envío del **mensaje \_ LINE LINEDEVSTATE** se puede controlar con [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Una aplicación puede indicar cambios en los elementos de estado sobre los que desea recibir una notificación. De forma predeterminada, todos los informes de estado están deshabilitados, excepto LINEDEVSTATE \_ REINIT, que no se puede deshabilitar. Este mensaje se envía a todas las aplicaciones que tienen un identificador a la línea, incluidas aquellas que llamaron [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con el parámetro *dwPrivileges* establecido en LINECALLPRIVILEGE \_ NONE, LINECALLPRIVILEGE \_ OWNER, LINECALLPRIVILEGE MONITOR o combinaciones permitidas \_ de estas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ CREATE**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




