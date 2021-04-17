---
description: Realice una copia de seguridad de los volúmenes mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes. Minimice el tiempo de inactividad de la aplicación mediante la creación rápida de una instantánea (instantánea) de un volumen que duplique todos los datos. Realice una copia de seguridad multivolumen.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696476"
---
# <a name="volume-shadow-copy-service"></a>Servicio de instantáneas de volumen

## <a name="purpose"></a>Propósito

El Servicio de instantáneas de volumen (VSS) es un conjunto de interfaces COM que implementa un marco para permitir la realización de copias de seguridad de volumen mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes.

Para obtener una introducción a VSS para los administradores del sistema, consulte [servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service) en la biblioteca de TechNet.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

VSS es compatible con Microsoft Windows XP y versiones posteriores. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, consulte la sección de requisitos de la documentación de ese elemento.

Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 bits o de 64 bits. No se admite su ejecución en WOW64. Para obtener más información, vea [configuraciones y restricciones admitidas](usage-conventions.md).

**Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes de VSS de 32 bits bajo WOW64, pero no para copias de seguridad de estado del sistema. No se admite la ejecución de proveedores y escritores de VSS de 32 bits en WOW64. Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.

> [!Note]  
> Una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 no se puede usar en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008. Una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 no se puede usar en un equipo que ejecute Windows Server 2003. Sin embargo, una instantánea creada en Windows Server 2008 puede usarse en un equipo que ejecute Windows Server 2008 R2 y viceversa.

 

## <a name="in-this-section"></a>En esta sección



| Tema                                                          | Descripción                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Información general](volume-shadow-copy-service-overview.md)<br/> | Describe el modelo de objetos de VSS, las estrategias de copia de seguridad y restauración, y cómo crear proveedores, solicitantes y escritores de VSS.<br/> |
| [Referencia](volume-shadow-copy-reference.md)<br/>       | Describe las clases, los tipos de datos, las enumeraciones, las funciones, las interfaces y las estructuras de VSS.<br/>                                  |



 

## <a name="additional-resources"></a>Recursos adicionales



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista y versiones posteriores            | VSS está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows. Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=8279). También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el centro de descarga de Windows. Las versiones anteriores del SDK se pueden descargar desde la [Página de descarga de Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx). |
| Windows Server 2003 y Windows XP | VSS está disponible en el SDK de Servicio de instantáneas de volumen 7,2, que se puede descargar desde el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=23490). Tenga en cuenta que los archivos vssapi. lib de 64 bits en los directorios del \\ directorio obj de Win2003 se pueden usar para las versiones de 64 bits de Windows Server 2003 y Windows XP.                                                                                                                                                                 |



 

 

 
