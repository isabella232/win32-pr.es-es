---
description: Evolución de la compatibilidad de MUI entre versiones de Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evolución de la compatibilidad de MUI entre versiones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687772"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Evolución de la compatibilidad de MUI entre versiones de Windows

-   [Antes de Windows Vista](#before-windows-vista)
-   [Windows Vista y versiones posteriores](#windows-vista-and-beyond)
    -   [Un sistema operativo independiente de idioma o MUI](#a-language-neutralmui-operating-system)
    -   [Los escenarios de implementación están totalmente basados en MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Implementación de una sola imagen](#single-image-deployment)
    -   [Modelo de servicio mejorado](#improved-servicing-model)
    -   [Infraestructura de MUI](#mui-infrastructure)
    -   [Administración de idiomas](#language-management)
    -   [Administración de recursos](#resource-handling)

## <a name="before-windows-vista"></a>Antes de Windows Vista

Antes de la versión de Windows Vista, Windows se incluía con imágenes de un solo idioma, lo que significaba que cada versión localizada de Windows contenía un solo idioma para su interfaz de usuario. MUI era un complemento para la versión en inglés del sistema operativo y los paquetes de interfaz de usuario multilingüe solo se podían agregar a determinadas versiones en Inglés de Windows. Cuando se instala en la versión en Inglés de Windows, MUI permitía cambiar el idioma de la interfaz de usuario del sistema operativo según las preferencias de los usuarios individuales a uno de los idiomas admitidos.

El modelo de paquete MUI no expondría la compatibilidad de MUI con las aplicaciones. Aunque los desarrolladores pueden crear aplicaciones multilingües, tenían que crear sus propios mecanismos para hacerlo.

## <a name="windows-vista-and-beyond"></a>Windows Vista y versiones posteriores

Con Windows Vista, Microsoft ha realizado una inversión importante en MUI. Windows Vista se crea desde el principio en una plataforma MUI. Aunque esto representa un avance importante en la estrategia de localización de Windows, ya que es un componente clave para que Microsoft proporcione Windows en más idiomas que nunca, es primero y más importante para los usuarios y clientes de Windows.

### <a name="a-language-neutralmui-operating-system"></a>Un sistema operativo independiente de idioma o MUI

La gran mayoría de los binarios de Windows Vista son compatibles con MUI y sus datos localizables se almacenan de forma independiente del código. Esto ofrece flexibilidad, ya que se pueden agregar datos de idioma diferentes en cualquier momento.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Los escenarios de implementación están totalmente basados en MUI

El diseño de empaquetado e instalación de Windows Vista se basa en MUI y todos los datos localizables se empaquetan en paquetes específicos del idioma, y cada paquete de idioma se puede implementar en distintos escenarios. Por ejemplo, aunque los DVDs comerciales para Windows Vista contienen versiones de un solo idioma, los usuarios de la edición Ultimate pueden descargar paquetes de idioma MUI adicionales y pueden cambiar el idioma de la interfaz de usuario desde el panel de control **configuración regional y de idioma** . Los licencias de Enterprise Edition obtienen todos los idiomas y pueden implementar cualquiera de ellos.

### <a name="single-image-deployment"></a>Implementación de una sola imagen

Los OEM y los clientes de empresa ahora pueden reducir el número de imágenes que necesitan mantener para implementar Windows y las aplicaciones en equipos en diferentes configuraciones regionales a través de una implementación de imagen única.

Con MUI en Windows Vista, se puede implementar una imagen que contenga varios idiomas en cualquier usuario de idioma, y los usuarios pueden determinar sus propios idiomas preferidos (dentro de la Directiva) durante la instalación o la "configuración rápida" del equipo. En concreto, los OEM pueden colocar muchos idiomas de interfaz de usuario en sus nuevos equipos para permitir que los usuarios seleccionen uno en el centro de bienvenida. Por lo tanto, desde una imagen con varios paquetes de idioma, el programa de instalación mostrará una lista de idiomas disponibles y permitirá a los usuarios elegir uno de ellos. Toda la configuración internacional se establece para que coincida con el idioma o la configuración regional seleccionados.

### <a name="improved-servicing-model"></a>Modelo de servicio mejorado

El mismo paquete QFE o corrección de seguridad ahora se puede instalar sobre cualquier sistema de idioma. Esto es fundamental, ya que permite un procesamiento más rápido de las correcciones de seguridad en particular y permite a todos los usuarios internacionales beneficiarse de la misma disponibilidad de todas las correcciones de seguridad.

### <a name="mui-infrastructure"></a>Infraestructura de MUI

A partir de Windows Vista, las API de MUI están disponibles para que los desarrolladores puedan aprovechar las ventajas de los mecanismos de MUI para sus propias aplicaciones, sin tener que crear lógica personalizada para la administración de recursos y el control de los recursos.

### <a name="language-management"></a>Administración de idiomas

Las API de MUI de base que proporcionan capacidades de administración del idioma de la interfaz de usuario están disponibles como parte de la infraestructura de MUI. Para ayudar a administrar la configuración de idioma de interfaz de usuario diferente en el nivel de sistema, usuario y aplicación, MUI los combina internamente en una sola lista de prioridades. A continuación, MUI implementa un mecanismo de reserva basado en esta lista priorizada, lo que permite soluciones de localización parciales a la vez que se proporciona a los usuarios una experiencia de idioma de interfaz de usuario adecuada (si no se prefiere).

Por ejemplo, un sistema que ejecuta la versión en Español de Windows Vista con un paquete de interfaz de idiomas (LIP) de catalán instalado sobre el sistema operativo base puede admitir el comportamiento siguiente: el sistema probará y mostrará primero sus recursos en catalán, y si estos recursos no están disponibles en catalán, proporcione en su lugar el usuario con recursos en español.

### <a name="resource-handling"></a>Administración de recursos

Con la infraestructura de MUI mejorada que está disponible a partir de Windows Vista, la mayoría de las tecnologías de recursos comunes están habilitadas para MUI. En la tabla siguiente se proporcionan detalles adicionales sobre la compatibilidad con el control de recursos disponible en Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Soporte técnico</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipos de recurso admitidos</td>
<td><ul>
<li>Win32/recurso no administrado:. DLL/. EXE/. OCX</li>
<li>Registros relacionados con el shell</li>
<li>Recursos relacionados con la administración: registro de eventos, Complementos/archivos MSC</li>
<li>WMI: MOF/MFL</li>
<li>Directiva de grupo: ADMX/ADML</li>
<li>Resources.dll administrado</li>
</ul></td>
</tr>
<tr class="even">
<td>Herramientas de desarrollo</td>
<td><ul>
<li>Para Win32: RC.exe, MUIRCT.exe y Visual Studio 2005 y versiones posteriores</li>
</ul></td>
</tr>
<tr class="odd">
<td>Compatibilidad con tipos de recursos limitados</td>
<td><ul>
<li>archivos de ayuda *. chm</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



