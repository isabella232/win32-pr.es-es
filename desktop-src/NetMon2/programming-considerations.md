---
description: Este tema contiene información de programación. La lista siguiente identifica algunas sugerencias de programación para ayudarle a escribir un analizador.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Consideraciones de programación (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213104060f7dd3c6b6dbe56d22044508e0878c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813310"
---
# <a name="programming-considerations-network-monitor"></a>Consideraciones de programación (Monitor de red)

Este tema contiene información de programación. La lista siguiente identifica algunas sugerencias de programación para ayudarle a escribir un analizador.



|                                                 |                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instalación automática del analizador                     | Implemente la función [**ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar automáticamente el analizador y actualizar los archivos INI asociados. Si instala el analizador manualmente, debe actualizar manualmente todos los archivos INI asociados.                                                                                                                                                          |
| Analizar propiedades de protocolo                     | Implemente la función [**AttachProperties**](attachproperties.md) para analizar las propiedades del protocolo. Evite el uso de la función [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) cuando adjunte una instancia de propiedad y úsela solo para datos no alineados con bytes o datos que deban descodificarse. Adjuntar propiedades hace referencia a la asignación de una instancia de propiedad a una ubicación específica en una captura. |
| Analizar los protocolos que se dividen entre marcos | Supongamos que cada parte del protocolo está completa dentro de un marco y presupone que el usuario llama a la herramienta de fusión de protocolos para combinar las partes en un protocolo. No vuelva a mirar un fotograma anterior al analizar un protocolo y evite intentar reconstruir un protocolo que se divida entre fotogramas.                                                                                              |
| Aplicar formato a los datos mostrados                       | Llame a la función [**FormatPropertyInstance**](formatpropertyinstance.md) para usar el formateador genérico con el fin de dar formato a los datos mostrados en el panel de detalles de la interfaz de usuario de monitor de red. Evite escribir un formateador personalizado para los datos de presentación de la interfaz de usuario. Sin embargo, puede llamar a un formateador personalizado para crear una línea de [*propiedades de Resumen*](s.md) para el protocolo que está analizando.            |
| Usar CCAlloc                                   | Use CCAlloc cuando desee Monitor de red para asignar datos por captura. Monitor de red no especifica el orden en el que los marcos llaman al analizador.                                                                                                                                                                                                                                                |
| Mantener un analizador sin estado                      | Mantener sin estado la operación de analizador porque cuando Monitor de red analiza una captura, no pasa los fotogramas al analizador en un orden específico. Por esta razón, se recomienda no conservar los datos globales.                                                                                                                                                                                      |



 

 

 



