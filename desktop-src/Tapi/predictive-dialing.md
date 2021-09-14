---
description: La marcación predictiva es una aplicación que normalmente se ejecuta en un servidor de telefonía del centro de llamadas.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Marcado predictivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168862"
---
# <a name="predictive-dialing"></a>Marcado predictivo

La marcación predictiva es una aplicación que normalmente se ejecuta en un servidor de telefonía del centro de llamadas. Usa una lista de números de teléfono, a menudo obtenidos de una base de datos, para intentar llamadas salientes. cuando se completa una *llamada*, la llamada se asigna automáticamente a un agente para su control. La aplicación puede hacer  uso de un puerto de marcado predictivo en un conmutador, que es un dispositivo que puede realizar llamadas salientes y tiene capacidades especiales (a través de DSP, y así sucesivamente) para detectar los tonos de progreso de la llamada y otras indicaciones de estado de llamada. Cuando se realiza una llamada en un puerto de marcado predictivo, normalmente se transfiere automáticamente a otro dispositivo del conmutador cuando la llamada alcanza un estado determinado o tras la detección de un tipo de medio determinado. este dispositivo de destino puede ser una cola para los agentes que administran las llamadas salientes.

Las aplicaciones identifican que un dispositivo tiene funcionalidad de marcado predictivo mediante el bit LINEADDRCAPFLAGS \_ PREDICTIVEDIALER del **miembro dwAddrCapFlags** en [**LINEADDRESSCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) El **miembro dwPredictiveAutoTransferStates** de **LINEADDRESSCAPS** indica los estados en los que se puede usar el puerto de marcado predictivo para transferir automáticamente una llamada; si este miembro es cero, indica que la transferencia automática no está disponible y que es responsabilidad de la aplicación transferir llamadas explícitamente al detectar el estado de llamada adecuado (o el tipo de medio u otros criterios). Preferiblemente, los fabricantes de modificadores pondrán a disposición la transferencia automática y manual, y permitirán a las aplicaciones seleccionar el mecanismo preferido, pero los proveedores de servicios tendrían que modelar el comportamiento de los equipos heredados. Un único puerto de marcado predictivo (dispositivo o dirección de línea) puede admitir la realización de varias llamadas salientes simultáneamente, como indica el miembro **dwMaxNumActiveCalls** en **LINEADDRESSCAPS.** La funcionalidad de marcado predictivo también se puede hacer disponible en cualquier dispositivo, mediante un grupo compartido de procesadores de señal de marcado predictivo, que se une a la línea que se marca a petición.

Cuando la función [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) se usa en una línea capaz de marcar de forma predictiva (un puerto con el conjunto LINEADDRCAPFLAGS PREDICTIVEDIALER) y se solicita la marcación predictiva mediante \_ LINECALLPARAMFLAGS PREDICTIVEDIAL, la llamada se realiza de forma predictiva con la detección mejorada del progreso de la llamada \_ de color de voz. Se definen campos y constantes adicionales en la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) que se pasa a **lineMakeCall** para controlar el comportamiento del puerto de marcado predictivo. El **miembro dwPredictiveAutoTransferStates** indica que, tras la entrada de la llamada a cualquiera de ellos, el puerto de marcado predictivo debe transferir automáticamente la llamada al destino designado (los bits deben ser un subconjunto adecuado de los estados de transferencia automática admitidos indicados en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)); La aplicación puede dejar el campo establecido en 0 si desea supervisar los estados de llamada y usar [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) para transferir la llamada cuando alcance la condición deseada. La aplicación debe especificar la dirección deseada a la que se debe transferir automáticamente la llamada en el campo de variable definido por los miembros **dwTargetAddressSize** y **dwTargetAddressOffset** en **LINECALLPARAMS.**

Las aplicaciones también pueden establecer un tiempo de espera para las llamadas salientes para que el proveedor de servicios las transición automáticamente a un estado desconectado si no se responden. Esto se controla mediante el **miembro dwNoAnswerTimeout** en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).

 

 



