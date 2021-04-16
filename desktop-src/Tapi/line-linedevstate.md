---
description: El \_ mensaje de línea de LINEDEVSTATE TAPI se envía cuando cambia el estado de un dispositivo de línea. La aplicación puede invocar lineGetLineDevStatus para determinar el nuevo estado de la línea.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Mensaje de LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690315"
---
# <a name="line_linedevstate-message"></a>Mensaje de línea \_ LINEDEVSTATE

El mensaje de **línea de \_ LINEDEVSTATE** TAPI se envía cuando cambia el estado de un dispositivo de línea. La aplicación puede invocar [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) para determinar el nuevo estado de la línea.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del dispositivo de línea. Este parámetro es **null** cuando *dwParam1* es LINEDEVSTATE \_ reinit.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea. Si el parámetro *dwParam1* es LINEDEVSTATE \_ reinit, el parámetro *dwCallbackInstance* no es válido y se establece en cero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

El elemento de estado de dispositivo de línea que ha cambiado. El parámetro puede ser una o varias de las [**\_ constantes LINEDEVSTATE**](linedevstate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

La interpretación de este parámetro depende del valor de *dwParam1*. Si *dwParam1* es LINEDEVSTATE \_ Ringing, *dwParam2* contiene el modo de anillo con el que el modificador indica a la línea que suene. Los modos de anillo válidos son números en el intervalo de uno a **dwNumRingModes**, donde **dwNumRingModes** es una funcionalidad de dispositivo de línea.

Si *dwParam1* es LINEDEVSTATE \_ reinit y TAPI emitió el mensaje como resultado de la conversión de un nuevo mensaje de API en un mensaje de reinicialización, *DwParam2* contiene el parámetro *dwMsg* del mensaje original (por ejemplo, [**line \_ Create**](line-create.md) o line \_ LINEDEVSTATE). Si *dwParam2* es cero, indica que el mensaje de reinicialización es un mensaje de reinicialización "real" que requiere que la aplicación llame a [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) lo antes posible.

</dd> <dt>

*dwParam3* 
</dt> <dd>

La interpretación de este parámetro depende del valor de *dwParam1*. Si *dwParam1* es LINEDEVSTATE \_ Ringing, *dwParam3* contiene el recuento de anillos para este evento de anillo. El número de anillos comienza en cero.

Si *dwParam1* es LINEDEVSTATE \_ reinit y TAPI emitió el mensaje como resultado de la conversión de un nuevo mensaje de API en un mensaje de reinicialización, *DwParam3* contiene el parámetro *dwParam1* del mensaje original (por ejemplo, LINEDEVSTATE \_ TRANSLATECHANGE o algún otro \_ valor LINEDEVSTATE, si *dwParam2* es la línea \_ LINEDEVSTATE o el nuevo identificador de dispositivo, si *dwParam2* es [**line \_ Create**](line-create.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El envío del mensaje **line \_ LINEDEVSTATE** se puede controlar con [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Una aplicación puede indicar cambios en el elemento de estado sobre los que desea recibir notificaciones. De forma predeterminada, todos los informes de estado se deshabilitan, excepto LINEDEVSTATE \_ reinit, que no se puede deshabilitar. Este mensaje se envía a todas las aplicaciones que tienen un identificador a la línea, incluidos los que llaman a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con el parámetro *DWPRIVILEGES* establecido en LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ monitor o las combinaciones permitidas de estos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**cierre de línea \_**](line-close.md)
</dt> <dt>

[**creación de línea \_**](line-create.md)
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

 

 




