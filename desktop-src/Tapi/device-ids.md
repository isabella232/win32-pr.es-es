---
description: Otras funciones de teléfono TAPI usan un identificador para un dispositivo de teléfono abierto para identificar el dispositivo de teléfono abierto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: Identificadores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51363d5b5de2ee45858c5500231ef2b9840087160574e9884958fb724328932e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867397"
---
# <a name="device-ids"></a>Identificadores de dispositivo

Otras funciones de teléfono TAPI usan un identificador para un dispositivo de teléfono abierto para identificar el dispositivo de teléfono abierto. Las únicas funciones para dispositivos de teléfono que toman un parámetro de identificador de dispositivo de teléfono (en lugar de un identificador de teléfono) son las funciones [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) y [**phoneOpen.**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) Una aplicación puede recuperar el identificador de dispositivo del teléfono mediante la [**función phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) con el identificador de teléfono como parámetro.

Una aplicación también puede obtener identificadores de dispositivo para varias clases de dispositivo asociadas a un teléfono abierto mediante la invocación [**de phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid). Consulte [Clases de dispositivo TAPI para](tapi-device-classes.md) obtener los nombres de clase de dispositivo.

Esta función toma un identificador de teléfono y una descripción de clase de dispositivo. Devuelve el identificador de dispositivo para el dispositivo de la clase de dispositivo determinada que está asociada al dispositivo de teléfono abierto. Si la clase de dispositivo es "tapi/phone", se devuelve el identificador de dispositivo del dispositivo de teléfono.

A diferencia de los dispositivos de línea, para los que los servicios de línea básicos proporcionan el equivalente de JARS, no se define ningún conjunto mínimo garantizado de funciones para dispositivos de teléfono. Aunque cada dispositivo de teléfono proporciona al menos las funciones y los mensajes descritos en esta sección, no ofrecen ninguna operación real en el dispositivo de teléfono físico.

 

 



