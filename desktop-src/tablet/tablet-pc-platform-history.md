---
description: En esta sección se describe el historial de versiones de la tecnología de Tablet PC.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Historial de la plataforma de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f258876f79f8e701ed59242233dcccc292b15f52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083313"
---
# <a name="tablet-pc-platform-history"></a>Historial de la plataforma de Tablet PC

En esta sección se describe el historial de versiones de la tecnología de Tablet PC.

## <a name="platform-description"></a>Descripción de la plataforma

Los componentes de tecnología de Tablet PC permiten desarrollar aplicaciones diseñadas para el hardware de Tablet PC.

Estos componentes se pueden usar para compilar aplicaciones que se ejecutan en Windows XP Tablet PC Edition 2005, Windows Vista, Windows 7, Windows Server 2008 R2 y otros sistemas operativos anteriores.

La Windows Presentation Foundation también admite el desarrollo de aplicaciones de Tablet PC.

## <a name="version-history"></a>Historial de versiones

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Plataforma de tableta en Windows 7 y Windows Server 2008 R2

Windows 7 incluye compatibilidad con lenguajes adicionales, el control de entrada matemática y diccionarios personalizados. Las características de [Windows Touch](../wintouch/windows-touch-portal.md) también se han agregado a los sistemas operativos Windows.

Windows Server 2008 R2 incorpora compatibilidad para idiomas adicionales, diccionarios personalizados y reconocimiento del lado servidor.

Las siguientes características mejoran la funcionalidad de Tablet PC y permiten a los desarrolladores ofrecer nuevas aplicaciones que admiten escenarios prácticos para los usuarios finales.

-   El control de entrada matemática permite la entrada de fórmulas y funciones matemáticas desde texto manuscrito en Windows 7.
-   En un esfuerzo por mejorar el reconocimiento de texto, Windows 7 y Windows Server 2008 R2 admiten diccionarios personalizados para que los administradores puedan habilitar directamente la compatibilidad con las listas de palabras.
-   Windows Touch admite la entrada de varios orígenes táctiles a través de mensajes de ventana nuevos, además de una API de reconocimiento de gestos que admite la panorámica, el zoom y la rotación.
-   Windows Server 2008 R2 admite el reconocimiento del servidor de la entrada del formulario y también admite diccionarios personalizados para el reconocimiento del lado servidor. Con la adición de estas características, los desarrolladores y los administradores pueden crear y personalizar aplicaciones eficaces que admitan el reconocimiento de escritura a mano desde el lado servidor.

### <a name="tablet-platform-in-windows-vista"></a>Plataforma de tableta en Windows Vista

Los archivos binarios de tecnología de Tablet PC se han actualizado en Windows Vista. La tecnología de Tablet PC actualizada incluye nuevas API de análisis de tinta y una versión COM de las API de entrada del lápiz. Las aplicaciones escritas en versiones anteriores de la tecnología de Tablet PC se ejecutan en Windows Vista sin modificarla.

Los componentes de tecnología de Tablet PC solo están disponibles como parte de la Windows SDK a partir de la versión de Windows Vista. Para obtener más información, vea [novedades en el desarrollo de Tablet PC](what-s-new-in-tablet-pc-development.md).

### <a name="version-17"></a>Versión 1,7

El kit de desarrollo de Tablet PC 1,7 amplió la funcionalidad de desarrollo más allá de la disponible en la versión 1,5, agregando las API de entrada del lápiz y la compatibilidad con la entrada de lápiz en la Web.

En el pasado, la funcionalidad de la versión 1,5 se encontraba en un archivo binario independiente, pero en el kit de desarrollo de Tablet PC 1,7, todas las funciones se colocaban en un solo binario.

### <a name="version-15"></a>Versión 1.5

Versión 1,5 del kit de desarrollo reemplazado por la versión 1,1. Proporcionaba las API del panel de entrada de lápiz y el objeto de divisor.

> [!Note]  
> Si instala el kit de desarrollo de Tablet PC versión 1,5, después de la instalación debe restablecer las referencias al ensamblado de Microsoft Ink en las aplicaciones escritas en versiones anteriores del SDK de Tablet PC antes de compilar y ejecutar.

 

### <a name="version-11"></a>Versión 1.1

Versión 1,1 del kit de desarrollo reemplazado por la versión 1,0. La versión 1,1 consta únicamente de las actualizaciones de la documentación; los archivos binarios de la plataforma no se cambiaron entre la versión 1,1 del kit de desarrollo y la versión distribuida de Windows XP Tablet PC Edition. Por lo tanto, las aplicaciones desarrolladas con el kit de desarrollo de la versión 1,1 no necesitan redistribuir los componentes para usar las características de la plataforma cuando se instalan en Tablet PC.

> [!Note]  
> Las aplicaciones que se distribuyen a sistemas operativos que no son de Tablet PC pueden usar un subconjunto de características de la plataforma de Tablet PC. Estas aplicaciones deben incluir el módulo de combinación redistribuida que se incluye en el kit de desarrollo de la versión 1,1 con su configuración.

 

### <a name="version-10"></a>Versión 1.0

La versión 1,0 del kit de desarrollo se ha sustituido por la versión 1,1.

 

 
