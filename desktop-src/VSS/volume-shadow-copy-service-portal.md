---
description: Copia de seguridad de volúmenes mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes. Minimice el tiempo de inactividad de la aplicación mediante la creación rápida de una instantánea (instantánea) de un volumen que duplica todos los datos. Realice una copia de seguridad multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443086"
---
# <a name="volume-shadow-copy-service"></a>Servicio de instantáneas de volumen

## <a name="purpose"></a>Propósito

El Servicio de instantáneas de volumen (VSS) es un conjunto de interfaces COM que implementa un marco para permitir realizar copias de seguridad de volúmenes mientras las aplicaciones de un sistema siguen escribiendo en los volúmenes.

Para obtener una introducción a VSS para administradores del sistema, [consulte Servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service) en la biblioteca de TechNet.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

VSS es compatible con Microsoft Windows XP y versiones posteriores. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la documentación de ese elemento.

Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 o 64 bits. No se admite su ejecución en WOW64. Para obtener más información, [vea Configuraciones y restricciones admitidas.](usage-conventions.md)

**Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes de VSS de 32 bits en WOW64, pero no para copias de seguridad de estado del sistema. No se admite la ejecución de escritores y proveedores de VSS de 32 bits en WOW64. Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.

> [!Note]  
> No se puede usar una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008. No se puede usar una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 en un equipo que ejecute Windows Server 2003. Sin embargo, una instantánea que se creó en Windows Server 2008 se puede usar en un equipo que ejecuta Windows Server 2008 R2 y viceversa.

 

## <a name="in-this-section"></a>En esta sección



| Tema                                                          | Descripción                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Información general](volume-shadow-copy-service-overview.md)<br/> | Describe el modelo de objetos de VSS, las estrategias de copia de seguridad y restauración, y cómo crear proveedores, solicitantes y escritores de VSS.<br/> |
| [Referencia](volume-shadow-copy-reference.md)<br/>       | Describe clases, tipos de datos, enumeraciones, funciones, interfaces y estructuras de VSS.<br/>                                  |



 

## <a name="additional-resources"></a>Recursos adicionales



|   Recurso                                 |   Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista y versiones posteriores            | VSS está disponible en microsoft Kit de desarrollo de software de Windows (SDK). Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el Centro [de descarga de Windows.](https://www.microsoft.com/download/details.aspx?id=8279) También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el Centro de descarga de Windows. Las versiones anteriores del SDK se pueden descargar desde la [Windows SDK descargar](https://msdn.microsoft.com/windows/bb980924.aspx). |
| Windows Server 2003 y Windows XP | VSS está disponible en el SDK Servicio de instantáneas de volumen 7.2, que puede descargar desde el Centro [de descarga de Windows.](https://www.microsoft.com/download/details.aspx?id=23490) Tenga en cuenta que los archivos vssapi.lib de 64 bits de los directorios del directorio Obj de Win2003 se pueden usar para las versiones de 64 bits de \\ Windows Server 2003 y Windows XP.                                                                                                                                                                 |



 

 

 
