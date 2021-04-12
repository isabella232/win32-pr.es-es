---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuevos archivos binarios de Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278218"
---
# <a name="new-low-level-binaries"></a>Nuevos archivos binarios de Low-Level

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : alta  











## <a name="description"></a>Descripción

Para mejorar las eficiencias de ingeniería internas y mejorar las bases de trabajo en el futuro, hemos reubicado alguna funcionalidad para los nuevos archivos binarios de bajo nivel. Esta refactorización hará posible que las instalaciones futuras de Windows proporcionen subconjuntos de funcionalidad para reducir el área expuesta (requisitos de disco y memoria, mantenimiento y superficie expuesta a ataques).

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Como ejemplo de funcionalidad que se ha migrado a archivos binarios de bajo nivel, kernelbase.dll obtiene la funcionalidad de kernel32.dll y advapi32.dll. Esto significa que el binario existente ahora reenvía las llamadas al nuevo binario en lugar de controlarlas directamente; el reenvío puede ser estático (la tabla de exportación muestra el redireccionamiento) o en tiempo de ejecución (el archivo dll tiene una rutina de código auxiliar que llama al nuevo binario). Esto afectará a las aplicaciones de bajo nivel como la seguridad y las aplicaciones de copia de seguridad que dependen de las API internas y los desplazamientos.

## <a name="solution"></a>Solución

El único impacto es el código que realiza suposiciones al intentar examinar el kernel32.dll o la advapi32.dll Exportar tabla en memoria, como puede ser una aplicación antivirus. Usar API publicadas y no los detalles de su implementación. Este es solo un ejemplo de la implementación en torno a un detalle de la implementación de una API.

 

 



