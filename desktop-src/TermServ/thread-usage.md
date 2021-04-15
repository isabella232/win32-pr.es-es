---
title: Uso de subprocesos
description: Debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno de Servicios de Escritorio remoto multiusuario y multiprocesador.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676117"
---
# <a name="thread-usage"></a>Uso de subprocesos

Los subprocesos proporcionan una forma cómoda de permitir que una aplicación maximice el uso de los recursos de CPU en un sistema, especialmente en una configuración de varios procesadores. Sin embargo, en un entorno de Servicios de Escritorio remoto, varios usuarios pueden ejecutar aplicaciones multiproceso y todos los subprocesos de todos los usuarios compiten por los recursos de CPU centrales de ese sistema. Teniendo esto en cuenta, debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno de Servicios de Escritorio remoto multiusuario y multiprocesador. Aunque una aplicación multiproceso mal diseñada con subprocesos inactivos o desperdiciados podría funcionar adecuadamente en un equipo cliente, la misma aplicación podría no funcionar bien en un servidor de Servicios de Escritorio remoto multiusuario.

 

 




