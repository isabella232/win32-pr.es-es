---
title: Uso de subprocesos
description: Debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno multiusuario y multiprocesador Servicios de Escritorio remoto aplicación.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22959c6950458c95670d71479a2efe04fdafea765048508b9bd371b0a215064d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869525"
---
# <a name="thread-usage"></a>Uso de subprocesos

Los subprocesos proporcionan una manera cómoda de permitir que una aplicación maximice su uso de recursos de CPU en un sistema, especialmente en una configuración de varios procesadores. Sin embargo, en un entorno de Servicios de Escritorio remoto, varios usuarios pueden ejecutar aplicaciones multiproceso y todos los subprocesos de todos los usuarios compiten por los recursos de CPU centrales de ese sistema. Con esto en mente, debe optimizar y equilibrar el uso de subprocesos de aplicación para un entorno multiusuario y multiprocesador Servicios de Escritorio remoto aplicación. Aunque una aplicación multiproceso mal diseñada con subprocesos inactivos o desperdiciados puede tener un rendimiento adecuado en un equipo cliente, es posible que la misma aplicación no tenga un buen rendimiento en un servidor de Servicios de Escritorio remoto multiusuario.

 

 




