---
title: Datos arbitrarios personalizados Secuencias
description: Datos arbitrarios personalizados Secuencias
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows SDK de formato multimedia, flujos de datos arbitrarios personalizados
- Formato de sistemas avanzados (ASF), flujos de datos arbitrarios personalizados
- ASF (formato de sistemas avanzados), flujos de datos arbitrarios personalizados
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- flujos de datos arbitrarios personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572217"
---
# <a name="custom-arbitrary-data-streams"></a>Datos arbitrarios personalizados Secuencias

Puede crear una secuencia en un archivo ASF para que contenga cualquier tipo de datos. Si ninguno de los tipos de flujo admitidos se adapta a sus necesidades, debe usar un flujo de datos arbitrario. El objeto de escritor controla un flujo de datos arbitrario igual que cualquier flujo sin comprimir; Los ejemplos están en paquetes y se combinan con los ejemplos de otras secuencias de la sección de datos del archivo. Por supuesto, solo una aplicación de lectura que se haya programado específicamente para tratar con el tipo arbitrario podrá controlar los datos después de que el objeto de lectura los entregue.

Un uso común de flujos de datos arbitrarios es para los datos multimedia codificados mediante un códec de terceros. Dado que los objetos de este SDK no interactúan directamente con códecs de terceros, la aplicación de escritura debe procesar los ejemplos con la parte de codificación del códec y pasar las muestras comprimidas al escritor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Datos arbitrarios Secuencias**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de parámetros arbitrarios personalizados Secuencias**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




