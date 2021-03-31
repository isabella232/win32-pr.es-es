---
description: Los programas de ejemplo de las secciones siguientes realizan operaciones que requieren que los pares de claves pública y privada estén disponibles para el cifrado y descifrado de archivos, mensajes y firmas.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contenedores de claves, claves y certificados necesarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817643"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Contenedores de claves, claves y certificados necesarios

Los programas de ejemplo de las secciones siguientes realizan operaciones que requieren que los [*pares de claves pública y privada*](../secgloss/p-gly.md) estén disponibles para el cifrado y descifrado de archivos, mensajes y firmas. Muchos de estos programas se compilarán, vincularán y ejecutarán pero producirán errores en tiempo de ejecución sin la existencia de [*contenedores de claves*](../secgloss/k-gly.md), claves, [*almacenes de certificados*](../secgloss/c-gly.md)y certificados adecuados en esos almacenes.

Además, algunos de los certificados del almacén MY deben tener algunas de sus propiedades extendidas establecidas.

La creación del contenedor de claves predeterminado necesario puede realizarse mediante la ejecución del programa en el [ejemplo C programa: creación de un contenedor de claves y generación de claves](example-c-program-creating-a-key-container-and-generating-keys.md). Tenga en cuenta que la creación de un contenedor de claves no genera automáticamente pares de claves pública y privada. Sin embargo, el programa de ejemplo crea el contenedor de claves y genera los pares de claves pública y privada.

Una vez generados los pares de claves pública y privada, los certificados de prueba que usan esas claves se pueden obtener de una [*entidad de certificación*](../secgloss/c-gly.md) (CA).

Algunos de los programas suponen que existen certificados con nombres de asunto específicos en mi almacén del sistema. En concreto, varios programas buscan certificados con los nombres de asunto "certificado de prueba completa" y "Hortense". Los nombres de asunto de los certificados se pueden cambiar en el código para que coincidan con los nombres de asunto de los certificados que existen en el almacén de certificados MY.

Ejecutar el programa de ejemplo del [programa C de ejemplo: si se enumeran los certificados de un almacén](example-c-program-listing-the-certificates-in-a-store.md) , se mostrarán todos los certificados de un almacén y todas las propiedades extendidas que se establezcan en esos certificados.

 

 
