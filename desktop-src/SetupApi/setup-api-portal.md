---
description: Instala controladores de dispositivos desde programas con un script de configuración y archivos INF. Escribir un programa de instalación para la configuración del dispositivo y la instalación del controlador. Esta API ya no se recomienda para la instalación de aplicaciones de software.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667604"
---
# <a name="setup-api"></a>API de configuración

## <a name="purpose"></a>Propósito

La API de instalación proporciona un conjunto de funciones que una aplicación de instalación llama para realizar operaciones de instalación.

## <a name="where-applicable"></a>Donde sea aplicable

Estas funciones de configuración están disponibles para desarrollar una aplicación de instalación. La API de instalación ya no debe usarse para instalar aplicaciones. En su lugar, use el [Windows Installer](/windows/desktop/Msi/windows-installer-portal)para desarrollar instaladores de aplicaciones. La API de instalación continúa utilizándose para instalar controladores de dispositivos.

La API de instalación está pensada para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Un desarrollador puede usar la API de instalación si su aplicación de instalación requiere la siguiente funcionalidad:

-   Puesta en cola de archivos.
-   Instalación de archivos.
-   Control de los errores de instalación y solicitud de medios.
-   Actualizando entradas del registro.
-   Registro de archivos a medida que se instalan.
-   Almacenamiento de las rutas de acceso de origen usadas más recientemente.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener información acerca de los sistemas operativos necesarios para usar una función determinada, consulte la sección de requisitos de la documentación de la función.

## <a name="in-this-section"></a>En esta sección



| Tema                                 | Descripción                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [Información general](overview.md)<br/>   | Información general sobre la API de instalación.<br/>                                             |
| [Referencia](reference.md)<br/> | Documentación de los tipos de datos, las estructuras, las funciones y las notificaciones de la API de instalación.<br/> |



 

 

