---
title: Administrador de reinicio
description: Escriba instaladores personalizados para eliminar los reinicios del sistema necesarios para completar la actualización de un archivo en uso. Apague y reinicie todos los servicios del sistema, menos los críticos, de los programas.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Reinicio del administrador de reinicio de Mgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67910428fb781a5ddf8e2c719d30f2f0488e11d6b07daad1770788e8ad5f5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010103"
---
# <a name="restart-manager"></a>Administrador de reinicio

## <a name="purpose"></a>Propósito

La API de Restart Manager puede eliminar o reducir el número de reinicios del sistema necesarios para completar una instalación o actualización. La razón principal por la que las actualizaciones de software requieren un reinicio del sistema durante una instalación o actualización es que algunos de los archivos que se están actualizando están siendo usados actualmente por una aplicación o servicio en ejecución. El Administrador de reinicio permite apagar y reiniciar todos los [servicios](critical-system-services.md) del sistema, menos los críticos. Esto libera los archivos que están en uso y permite que se completen las operaciones de instalación.

## <a name="where-applicable"></a>Donde sea aplicable

El archivo DLL del Administrador de reinicio exporta una interfaz C pública que pueden cargar los instaladores estándar o personalizados. El instalador puede usar el Administrador de reinicio para registrar los archivos que se deben reemplazar durante la instalación de una aplicación o actualización. Después, durante una actualización o instalación posteriores, el instalador puede usar el Administrador de reinicio para determinar qué archivos no se pueden actualizar porque están en uso actualmente. El Administrador de reinicio puede apagar y reiniciar los servicios no críticos o las aplicaciones que actualmente usan esos archivos. Los instaladores pueden dirigir al Administrador de reinicio para que apague y reinicie aplicaciones o servicios en función del archivo en uso, el identificador de proceso (PID) o el nombre corto de un Windows servicio.

Restart Manager está pensado para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está pensada para desarrolladores de aplicaciones de instalación que desean aprovechar las funcionalidades del instalador en Windows Vista o Windows Server 2008. Las aplicaciones que usan [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versión 4.0 para la instalación y el mantenimiento usan automáticamente el Administrador de reinicio para reducir los reinicios del sistema. Los instaladores personalizados también se pueden diseñar para llamar a la API de Restart Manager para apagar y reiniciar aplicaciones y servicios. En los casos en los que un reinicio del sistema es inevitable, los instaladores pueden usar la API de Restart Manager para programar los reinicios de forma que minimice la interrupción del flujo de trabajo del usuario.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de Restart Manager está disponible a partir de Windows Vista y Windows Server 2008. Restart Manager consta de un único archivo DLL que las aplicaciones pueden cargar para acceder a la API de Restart Manager.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [Acerca del Administrador de reinicio](about-restart-manager.md)<br/>         | Temas de información general que describen el Administrador de reinicio.<br/>   |
| [Uso del Administrador de reinicio](using-restart-manager.md)<br/>         | Temas de información general sobre el uso de la API de Restart Manager.<br/> |
| [Referencia de Restart Manager](restart-manager-reference.md)<br/> | Temas de referencia de la API de Restart Manager.<br/>        |



 

 

