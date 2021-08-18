---
description: Nuevos Low-Level binarios
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuevos Low-Level binarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c84601fd1394c9e31123415953e87ef1beb69e173d2744368daf58e9f79355f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994895"
---
# <a name="new-low-level-binaries"></a>Nuevos Low-Level binarios

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** alta  











## <a name="description"></a>Descripción

Para mejorar las eficiencias de ingeniería internas y mejorar las bases para el trabajo futuro, hemos reubicado algunas funcionalidades en nuevos archivos binarios de bajo nivel. Esta refactorización permitirá que futuras instalaciones de Windows proporcionen subconjuntos de funcionalidad para reducir el área de superficie (requisitos de disco y memoria, mantenimiento y superficie de ataque).

## <a name="manifestation-of-impact"></a>Demostración de impacto

Como ejemplo de funcionalidad que hemos movido a archivos binarios de bajo nivel, kernelbase.dll la funcionalidad de kernel32.dll y advapi32.dll. Esto significa que el binario existente ahora reenvía las llamadas al nuevo binario en lugar de controlarlas directamente; el reenvío puede ser estático (la tabla de exportación muestra el redireccionamiento) o en tiempo de ejecución (el archivo DLL tiene una rutina de código auxiliar que llama al nuevo binario). Esto afectará a las aplicaciones de bajo nivel, como las aplicaciones de seguridad y de copia de seguridad que dependen de las API internas y los desplazamientos.

## <a name="solution"></a>Solución

El único impacto es el código que realiza suposiciones al intentar ver la tabla de exportación kernel32.dll o advapi32.dll en memoria, como una aplicación antivirus. Use las API publicadas y no los detalles de su implementación. Este es solo un ejemplo de implementación en torno a un detalle de implementación para una API.

 

 



