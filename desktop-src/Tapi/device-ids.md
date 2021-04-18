---
description: Otras funciones de teléfono TAPI usan un controlador para un dispositivo telefónico abierto para identificar el dispositivo telefónico abierto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: Identificadores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677385"
---
# <a name="device-ids"></a>Identificadores de dispositivo

Otras funciones de teléfono TAPI usan un controlador para un dispositivo telefónico abierto para identificar el dispositivo telefónico abierto. Las únicas funciones de los dispositivos telefónicos que toman un parámetro de identificador de dispositivo de teléfono (en lugar de un identificador de teléfono) son las funciones [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) y [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) . Una aplicación puede recuperar el identificador de dispositivo del teléfono mediante la función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) con el identificador de teléfono como parámetro.

Una aplicación también puede obtener identificadores de dispositivo para varias clases de dispositivos asociadas a un teléfono abierto mediante la invocación de [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid). Vea [clases de dispositivos TAPI](tapi-device-classes.md) para nombres de clase de dispositivo.

Esta función toma un identificador de teléfono y una descripción de clase de dispositivo. Devuelve el identificador de dispositivo del dispositivo de la clase de dispositivo especificada que está asociada con el dispositivo telefónico abierto. Si la clase de dispositivo es "TAPI/teléfono", se devuelve el identificador de dispositivo del dispositivo telefónico.

A diferencia de los dispositivos de línea, para los que los servicios de línea básicos proporcionan el equivalente de los POTS, no se define ningún conjunto de funciones mínimo garantizado para los dispositivos de teléfono. Aunque cada dispositivo telefónico proporciona al menos las funciones y los mensajes que se describen en esta sección, no ofrecen ninguna operación real en el dispositivo de teléfono físico.

 

 



