---
description: El marcado predictivo es una aplicación que normalmente se ejecuta en un servidor de telefonía del centro de llamadas.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Marcado predictivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678240"
---
# <a name="predictive-dialing"></a>Marcado predictivo

El marcado predictivo es una aplicación que normalmente se ejecuta en un servidor de telefonía del centro de llamadas. Usa una lista de números de teléfono, a menudo obtenidos de una base de datos, para intentar llamadas salientes. Cuando se *completa* una llamada, la llamada se asigna automáticamente a un agente para el control. La aplicación puede hacer uso de un *Puerto de marcado predictivo* en un conmutador, que es un dispositivo que puede realizar llamadas salientes y tiene capacidades especiales (a través de DSP, etc.) para detectar tonos de progreso de la llamada y otras indicaciones sonoras del estado de la llamada. Cuando se realiza una llamada en un puerto de marcado predictivo, normalmente se transfiere automáticamente a otro dispositivo del conmutador cuando la llamada alcanza un estado determinado o cuando se detecta un tipo de medio determinado. Este dispositivo de destino puede ser una cola de agentes que controlan las llamadas salientes.

Las aplicaciones identifican un dispositivo como con funcionalidad de marcado predictivo por el \_ bit LINEADDRCAPFLAGS PREDICTIVEDIALER en el miembro **DwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). El miembro **dwPredictiveAutoTransferStates** de **LINEADDRESSCAPS** indica los Estados en los que se puede hacer que el puerto de marcado predictivo transfiera automáticamente una llamada. Si este miembro es cero, indica que la transferencia automática no está disponible y que es responsabilidad de la aplicación transferir llamadas explícitamente al detectar el estado de llamada adecuado (o tipo de medio u otros criterios). Preferiblemente, los fabricantes de conmutadores harán que las transferencias automáticas y manuales estén disponibles y permitan que las aplicaciones seleccionen el mecanismo preferido, pero los proveedores de servicios tendrían que modelar el comportamiento de los equipos heredados. Un único puerto de marcado de predicción (dirección/dispositivo de línea) puede permitir realizar varias llamadas salientes simultáneamente, como indica el miembro **dwMaxNumActiveCalls** en **LINEADDRESSCAPS**. La capacidad de marcado predictivo también puede estar disponible en cualquier dispositivo, mediante un grupo compartido de procesadores de señal de marcación de predicción, que se conectan a la línea que se marca según la solicitud.

Cuando la función [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) se usa en una línea capaz de marcado predictivo (un puerto con el \_ conjunto PREDICTIVEDIALER LINEADDRCAPFLAGS) y se solicita el marcado predictivo mediante LINECALLPARAMFLAGS \_ PREDICTIVEDIAL, la llamada se realiza de forma predecible con la detección mejorada del progreso de la llamada. Los campos y las constantes adicionales se definen en la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) que se pasa a **lineMakeCall** para controlar el comportamiento del puerto de marcado predictivo. El miembro **dwPredictiveAutoTransferStates** indica la llamada de línea que, una vez realizada la llamada a cualquiera de ellas, el puerto de marcado predictivo debe transferir automáticamente la llamada al destino designado (los bits deben ser un subconjunto adecuado de los Estados de transferencia automática admitidos indicados en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)); la aplicación puede dejar el campo establecido en 0 si desea supervisar los Estados de llamada en sí y usar [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) para transferir la llamada cuando alcance la condición deseada. La aplicación debe especificar la dirección deseada a la que se debe transferir automáticamente la llamada en el campo de variable definido por los miembros **dwTargetAddressSize** y **dwTargetAddressOffset** en **LINECALLPARAMS**.

Las aplicaciones también pueden establecer un tiempo de espera para las llamadas salientes para que el proveedor de servicios las cambie automáticamente a un estado desconectado Si no se responde. Esto se controla mediante el miembro **dwNoAnswerTimeout** en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).

 

 



