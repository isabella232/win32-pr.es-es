---
title: La marca de prueba
description: La marca de prueba
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801494"
---
# <a name="the-test-flag"></a>La marca de prueba

La marca "test" (MCI TEST) consulta al \_ dispositivo para determinar si puede ejecutar el comando. El dispositivo devuelve un error si no puede ejecutar el comando. No devuelve ningún error si puede controlar el comando. Al especificar esta marca, MCI devuelve el control a la aplicación sin ejecutar el comando .

Esta marca es compatible con los dispositivos de vídeo digital y VCR para todos los comandos excepto [**open**](open.md) [**(MCI \_ OPEN)**](mci-open.md)y [**close**](close.md) ([**MCI \_ CLOSE**](mci-close.md)).

 

 




