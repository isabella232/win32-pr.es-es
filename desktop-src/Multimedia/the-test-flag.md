---
title: La marca de prueba
description: La marca de prueba
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260663"
---
# <a name="the-test-flag"></a>La marca de prueba

La marca "test" (MCI TEST) consulta al \_ dispositivo para determinar si puede ejecutar el comando. El dispositivo devuelve un error si no puede ejecutar el comando. No devuelve ningún error si puede controlar el comando. Al especificar esta marca, MCI devuelve el control a la aplicación sin ejecutar el comando .

Esta marca es compatible con los dispositivos de vídeo digital y VCR para todos los comandos excepto [**open**](open.md) [**(MCI \_ OPEN)**](mci-open.md)y [**close**](close.md) ([**MCI \_ CLOSE**](mci-close.md)).

 

 




