---
description: Un proveedor de alto rendimiento wmi aumenta considerablemente la velocidad a la que un cliente WMI puede obtener información de un proveedor de instancias wmi.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Mejora de la eficacia de un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d166cdc4817068363eec899a010c778b4fa125fbfb4eda11b2745558886be4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318819"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a>Mejora de la eficacia de un proveedor de instancias

Un proveedor de alto rendimiento wmi aumenta considerablemente la velocidad a la que un cliente WMI puede obtener información de un proveedor de instancias wmi. El cambio principal es que un proveedor de alto rendimiento se ejecuta como un servidor en proceso para la aplicación cliente o para WMI. Al colocar el proveedor dentro del proceso de cliente, puede acelerar la interacción entre los dos.

Para obtener más información sobre cómo convertir el proveedor de instancias en un proveedor de alto rendimiento, vea Convertir un proveedor de instancias en un [High-Performance de instancias.](making-an-instance-provider-into-a-high-performance-provider.md)

 

 



