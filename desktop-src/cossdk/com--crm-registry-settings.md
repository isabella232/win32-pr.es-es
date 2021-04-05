---
description: Hay varias opciones de configuración del registro disponibles para modificar el comportamiento de CRM para ayudar en la solución de problemas y el desarrollo.
ms.assetid: c4e68451-fb8a-45b5-9968-7d5a6418dfe8
title: Configuración del registro de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0ea4ec245ab55b73c79660973824fcf33c6c2b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907100"
---
# <a name="com-crm-registry-settings"></a>Configuración del registro de COM+ CRM

Hay varias opciones de configuración del registro disponibles para modificar el comportamiento de CRM para ayudar en la solución de problemas y el desarrollo. Todos estos valores del registro, que se enumeran y describen en la tabla siguiente, son opcionales; no se requiere ninguno para el funcionamiento normal de CRM.

La configuración del registro de CRM está en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ COM3 \\ CRM**. Cree la clave de **CRM** en la clave **COM3** si aún no está allí.



| Configuración del registro de CRM                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VTRACE1**<br/>                 | Valor de REG \_ DWORD. Si se establece en un valor distinto de cero, se habilitan los mensajes de seguimiento de depuración en advertencias o errores. Estos mensajes pueden verse en la ventana de salida del depurador. Este valor debe establecerse solo para el desarrollo y no durante la implementación normal. Este valor se lee cuando se inicia una aplicación de servidor CRM.<br/>                                                                                                                                                                                                                                                   |
| **IgnoreCompensatorErrors**<br/> | Valor de REG \_ DWORD. Si se establece este valor en un valor distinto de cero, la infraestructura de CRM omitirá todos los errores devueltos por los compensadores de CRM. Si se produce un error en la recuperación debido a un error de un compensador de CRM, el establecimiento de este valor permite que se complete la recuperación. Este valor se lee cuando se inicia una aplicación de servidor CRM.<br/>                                                                                                                                                                                                                                           |
| **CheckpointIntervalInSec**<br/> | Valor de REG \_ DWORD. Este es el intervalo de puntos de control en segundos. El intervalo de puntos de control predeterminado es de 30 segundos. Los puntos de control se usan para recuperar espacio del archivo de registro de CRM. Aumentar el intervalo de punto de comprobación puede aumentar el rendimiento, pero a costa de un aumento del tiempo de recuperación y un archivo de registro de CRM más grande. Este valor se lee cuando se inicia una aplicación de servidor CRM.<br/>                                                                                                                                                                                                  |
| **InitialLogFileSizeInKB**<br/>  | Valor de REG \_ DWORD. Es el tamaño inicial del archivo de registro de CRM en kilobytes. El tamaño predeterminado del archivo de registro de CRM es 1024 KB (1 MB). El archivo de registro de CRM se expande automáticamente para satisfacer la carga de transacciones impuesta en él, pero si se prevén cargas pesadas, es posible que sea necesario aumentar este valor. Este valor se lee cuando se inicia una aplicación de servidor COM+ habilitada para CRM, pero si el archivo de registro de CRM ya existe para una aplicación de servidor CRM, este valor se omite para esa aplicación de servidor.<br/>                                                                               |
| **RecoveryTraceEnabled**<br/>    | Valor de REG \_ DWORD. Si se establece en un valor distinto de cero, se habilita un seguimiento de recuperación. El seguimiento de recuperación es un archivo de texto que tiene el mismo nombre que el archivo de registro de CRM y la siguiente extensión adicional: .recoverytrace.txt. <br/> Este archivo se encuentra en el mismo directorio que el archivo de registro de CRM. El seguimiento de recuperación proporciona un seguimiento de la actividad de CRM durante la recuperación, que se puede usar para el diagnóstico de problemas. Este valor se lee cuando se inicia una aplicación de servidor CRM. Sin embargo, se genera un archivo de seguimiento de recuperación único para cada aplicación de servidor CRM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




