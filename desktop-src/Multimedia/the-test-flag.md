---
title: Marca de prueba
description: Marca de prueba
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357735"
---
# <a name="the-test-flag"></a>Marca de prueba

La marca "prueba" ( \_ prueba de MCI) consulta el dispositivo para determinar si puede ejecutar el comando. El dispositivo devuelve un error si no puede ejecutar el comando. No devuelve ningún error si puede controlar el comando. Cuando se especifica esta marca, MCI devuelve el control a la aplicación sin ejecutar el comando.

Esta marca es compatible con dispositivos digitales y vídeo VCR para todos los comandos excepto [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)) y [**cerrar**](close.md) ([**MCI \_ Close**](mci-close.md)).

 

 




