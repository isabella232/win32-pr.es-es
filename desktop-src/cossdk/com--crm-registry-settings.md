---
description: Hay varias configuraciones del Registro disponibles para modificar el comportamiento de CRM para ayudar con la solución de problemas y el desarrollo.
ms.assetid: c4e68451-fb8a-45b5-9968-7d5a6418dfe8
title: Registro de COM+ CRM Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0ea4ec245ab55b73c79660973824fcf33c6c2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465566"
---
# <a name="com-crm-registry-settings"></a>Registro de COM+ CRM Configuración

Hay varias configuraciones del Registro disponibles para modificar el comportamiento de CRM para ayudar con la solución de problemas y el desarrollo. Todas estas configuraciones del Registro, que se enumeran y describen en la tabla siguiente, son opcionales; no se requiere ninguno para el funcionamiento normal de CRM.

Toda la configuración del Registro de CRM se encuentra **en HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ COM3 \\ CRM**. Cree la **clave CRM** en la **clave COM3** si aún no está ahí.



| Configuración del Registro de CRM                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VTRACE1**<br/>                 | Valor \_ reg DWORD. Si se establece este valor en cualquier otro valor distinto de cero, se habilitan los mensajes de seguimiento de depuración en caso de advertencias o errores. Estos mensajes se pueden ver en la ventana de salida del depurador. Este valor debe establecerse solo para el desarrollo y no durante la implementación normal. Este valor se lee cuando se inicia cualquier aplicación de servidor CRM.<br/>                                                                                                                                                                                                                                                   |
| **IgnoreCompensatorErrors**<br/> | Valor \_ reg DWORD. Si se establece este valor en un valor distinto de cero, la infraestructura de CRM omitirá todos los errores devueltos por los compensadores de CRM. Si se produce un error en la recuperación debido a un error de un compensador crm, establecer este valor permite completar la recuperación. Este valor se lee cuando se inicia cualquier aplicación de servidor CRM.<br/>                                                                                                                                                                                                                                           |
| **CheckpointIntervalInSec**<br/> | Valor \_ reg DWORD. Este es el intervalo de punto de comprobación en segundos. El intervalo de punto de control predeterminado es de 30 segundos. Los puntos de control se usan para reclamar espacio del archivo de registro de CRM. Aumentar el intervalo de punto de control puede aumentar el rendimiento, pero a costa de un mayor tiempo de recuperación y un archivo de registro crm más grande. Este valor se lee cuando se inicia cualquier aplicación de servidor CRM.<br/>                                                                                                                                                                                                  |
| **InitialLogFileSizeInKB**<br/>  | Valor \_ reg DWORD. Este es el tamaño inicial del archivo de registro de CRM en kilobytes. El tamaño predeterminado del archivo de registro de CRM es de 1024 KB (1 MB). El archivo de registro de CRM se expande automáticamente para satisfacer la carga de transacciones que se le impone, pero si se prevén cargas pesadas, podría ser necesario aumentar este valor. Este valor se lee cuando se inicia cualquier aplicación de servidor COM+ habilitada para CRM, pero si el archivo de registro crm ya existe para una aplicación de servidor CRM, este valor se omite para esa aplicación de servidor.<br/>                                                                               |
| **RecoveryTraceEnabled**<br/>    | Valor \_ reg DWORD. Si se establece este valor en cualquier otro valor distinto de cero, se habilita un seguimiento de recuperación. El seguimiento de recuperación es un archivo de texto que tiene el mismo nombre que el archivo de registro crm y la siguiente extensión adicional: .recoverytrace.txt. <br/> Este archivo se encuentra en el mismo directorio que el archivo de registro de CRM. El seguimiento de recuperación proporciona un seguimiento de la actividad de CRM durante la recuperación, que se puede usar para el diagnóstico de problemas. Este valor se lee cuando se inicia cualquier aplicación de servidor CRM. Sin embargo, se genera un archivo de seguimiento de recuperación único para cada aplicación de servidor CRM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




