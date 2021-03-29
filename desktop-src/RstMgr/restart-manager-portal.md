---
title: Administrador de reinicio
description: Escriba instaladores personalizados para eliminar los reinicios del sistema necesarios para completar la actualización de un archivo en uso. Cierre y reinicie todos los servicios de sistema, pero críticos, de programas.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Admin. de reinicio del administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078089"
---
# <a name="restart-manager"></a>Administrador de reinicio

## <a name="purpose"></a>Propósito

La API del administrador de reinicio puede eliminar o reducir el número de reinicios del sistema necesarios para completar una instalación o actualización. La razón principal por la que las actualizaciones de software requieren un reinicio del sistema durante una instalación o actualización es que algunos de los archivos que se están actualizando se están usando actualmente en una aplicación o servicio en ejecución. El administrador de reinicio permite que todos los [servicios del sistema críticos](critical-system-services.md) se apaguen y se reinicien. Esto libera los archivos que se están usando y permite que se completen las operaciones de instalación.

## <a name="where-applicable"></a>Donde sea aplicable

El archivo DLL del administrador de reinicio exporta una interfaz pública de C que puede ser cargada por instaladores estándar o personalizados. El instalador puede usar el administrador de reinicio para registrar archivos que deben reemplazarse durante la instalación de una aplicación o una actualización. Después, durante una actualización o instalación posterior, el instalador puede usar el administrador de reinicio para determinar qué archivos no se pueden actualizar porque están actualmente en uso. El administrador de reinicio puede apagar y reiniciar los servicios no críticos o las aplicaciones que usan actualmente esos archivos. Los instaladores pueden dirigir el administrador de reinicio para apagar y reiniciar aplicaciones o servicios según el archivo en uso, el ID. de proceso (PID) o el nombre corto de un servicio de Windows.

El administrador de reinicio está diseñado para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está dirigida a los desarrolladores de aplicaciones de instalación que desean aprovechar las capacidades del instalador en Windows Vista o Windows Server 2008. Las aplicaciones que utilizan la [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versión 4,0 para la instalación y el mantenimiento usan automáticamente el administrador de reinicio para reducir los reinicios del sistema. Los instaladores personalizados también pueden diseñarse para que llamen a la API del administrador de reinicio para apagar y reiniciar las aplicaciones y los servicios. En los casos en los que no se puede evitar el reinicio del sistema, los instaladores pueden usar la API del administrador de reinicio para programar los reinicios de forma que se minimice la interrupción del flujo de trabajo del usuario.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API del administrador de reinicio está disponible a partir de Windows Vista y Windows Server 2008. El administrador de reinicio consta de un solo archivo DLL que las aplicaciones pueden cargar para tener acceso a la API del administrador de reinicio.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Acerca del administrador de reinicio](about-restart-manager.md)<br/>         | Temas de información general que describen el administrador de reinicio.<br/>   |
| [Uso del administrador de reinicio](using-restart-manager.md)<br/>         | Temas de información general sobre el uso de la API del administrador de reinicio.<br/> |
| [Referencia del administrador de reinicio](restart-manager-reference.md)<br/> | Temas de referencia de la API del administrador de reinicio.<br/>        |



 

 

