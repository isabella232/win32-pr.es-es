---
description: Este tema contiene información de programación. En la lista siguiente se identifican algunas sugerencias de programación para ayudarle a escribir un analizador.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Consideraciones de programación (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2deb53a27d8abda4f45663b65fb922600a5b5386
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120230"
---
# <a name="programming-considerations-network-monitor"></a>Consideraciones de programación (Monitor de red)

Este tema contiene información de programación. En la lista siguiente se identifican algunas sugerencias de programación para ayudarle a escribir un analizador.



| Sugerencia                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instalación automática del analizador                     | Implemente [**la función ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar automáticamente el analizador y actualizar los archivos INI asociados. Si instala el analizador manualmente, debe actualizar todos los archivos INI asociados manualmente.                                                                                                                                                          |
| Analizar las propiedades del protocolo                     | Implemente [**la función AttachProperties**](attachproperties.md) para analizar las propiedades del protocolo. Evite usar la [**función AttachPropertyInstanceEx**](attachpropertyinstanceex.md) al adjuntar una instancia de propiedad y úsela solo para datos no alineados con bytes o datos que deben descodificarse. La asociación de propiedades hace referencia a la asignación de una instancia de propiedad a una ubicación específica de una captura. |
| Análisis de protocolos que se dividen entre fotogramas | Suponga que cada parte del protocolo está completa dentro de un marco y suponga que el usuario llama a la herramienta Desenlace de protocolo para combinar las piezas en un solo protocolo. No mire hacia atrás en un marco anterior al analizar un protocolo y evite intentar reconstruir un protocolo dividido entre fotogramas.                                                                                              |
| Aplicación de formato a los datos mostrados                       | Llame a [**la función FormatPropertyInstance**](formatpropertyinstance.md) para usar el formateador genérico para dar formato a los datos mostrados en el panel de detalles de la interfaz Monitor de red usuario. Evite escribir un formateador personalizado para los datos de presentación de la interfaz de usuario. Sin embargo, puede llamar a un formateador personalizado para crear una línea de [*propiedades*](s.md) de resumen para el protocolo que está analizando.            |
| Uso de CCAlloc                                   | Use CCAlloc cuando desee asignar Monitor de red datos por captura. Monitor de red especifica el orden en que los fotogramas llaman al analizador.                                                                                                                                                                                                                                                |
| Mantener un analizador sin estado                      | Mantenga la operación del analizador sin estado porque cuando Monitor de red analiza una captura, no pasa los fotogramas al analizador en un orden específico. Por este motivo, se recomienda no conservar los datos globales.                                                                                                                                                                                      |



 

 

 



