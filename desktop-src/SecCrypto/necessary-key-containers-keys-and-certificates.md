---
description: Los programas de ejemplo de las secciones siguientes realizan operaciones que requieren que los pares de claves pública y privada estén disponibles para cifrar y descifrar archivos, mensajes y firmas.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contenedores de claves, claves y certificados necesarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173189"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Contenedores de claves, claves y certificados necesarios

Los programas de ejemplo de las [](../secgloss/p-gly.md) secciones siguientes realizan operaciones que requieren que los pares de claves pública y privada estén disponibles para cifrar y descifrar archivos, mensajes y firmas. Muchos de estos programas compilarán, vincularán y ejecutarán, pero se producirá un error en tiempo de ejecución sin la existencia de contenedores de [*claves,*](../secgloss/k-gly.md) [*claves,*](../secgloss/c-gly.md)almacenes de certificados y certificados adecuados en esos almacenes.

Además, algunos de los certificados del almacén MY deben tener algunas de sus propiedades extendidas establecidas.

Para crear el contenedor de claves predeterminado necesario, ejecute el programa en El programa [de ejemplo C: Crear](example-c-program-creating-a-key-container-and-generating-keys.md)un contenedor de claves y generar claves . Tenga en cuenta que la creación de un contenedor de claves no genera automáticamente pares de claves pública y privada. Sin embargo, el programa de ejemplo crea el contenedor de claves y genera los pares de claves pública y privada.

Una vez generados los pares de claves pública y privada, los certificados de prueba que usan esas claves se pueden obtener de una entidad [*de certificación*](../secgloss/c-gly.md) (CA).

Algunos de los programas asumen que existen certificados con nombres de firmantes específicos en el almacén del sistema MY. En concreto, varios programas buscan certificados con los nombres de sujeto "Certificado de prueba completa" y "Hortense". Los nombres de sujeto de los certificados se pueden cambiar en el código para que coincidan con los nombres de firmantes de los certificados que existen en el almacén de certificados MY.

Al ejecutar el programa de ejemplo en el Programa [de ejemplo C:](example-c-program-listing-the-certificates-in-a-store.md) al enumerar los certificados de un almacén se mostrarán todos los certificados de un almacén y todas las propiedades extendidas que se establecen en esos certificados.

 

 
