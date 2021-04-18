---
description: En esta sección se proporcionan instrucciones para integrar y extender las características orientadas al usuario de escritorio de Windows.
ms.assetid: 1ffeeb4f-b337-45b9-885f-307b81670557
title: Entorno de escritorio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb60457f700489ca4e9e7368425df380f8d10d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686748"
---
# <a name="desktop-environment"></a>Entorno de escritorio

En esta sección se proporcionan instrucciones para integrar y extender las características orientadas al usuario de escritorio de Windows. Puede obtener información sobre cómo asegurarse de que las aplicaciones y los formatos de archivo aparecen y se comportan correctamente en el inicio, en la barra de tareas, en el escritorio y en el explorador de archivos. También puede asegurarse de que los formatos de archivo y los almacenes de datos se pueden indexar y buscar.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Shell de Windows](./shell/shell-entry.md)<br/>                                      | La interfaz de usuario del escritorio de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo. El más conocido de estos objetos son las carpetas y los archivos que residen en las unidades de disco del equipo. También hay una serie de objetos virtuales que permiten al usuario realizar tareas como el envío de archivos a las impresoras remotas o el acceso a la papelera de reciclaje. El shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de obtener acceso a los objetos y administrarlos.<br/> |
| [Sistema de propiedades de Windows](./properties/windows-properties-system.md)<br/>         | El sistema de propiedades de Windows es un sistema de lectura y escritura extensible de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell. El sistema de propiedades de Windows permite almacenar y recuperar metadatos para los elementos de Shell. Un elemento de Shell es cualquier parte única de contenido, como un archivo, una carpeta, un correo electrónico o un contacto. Una propiedad es una parte individual de los metadatos asociados a un elemento de Shell.<br/>                                                                                                                                                                             |
| [Windows Search](./search/windows-search.md)<br/>                                 | Windows Search es una plataforma de búsqueda en el escritorio que tiene capacidades de búsqueda instantánea para la mayoría de los tipos de archivos y datos comunes, como correo electrónico, contactos, citas del calendario, documentos, fotos, multimedia y otros formatos que los desarrolladores de terceros pueden extender. Estas capacidades permiten a los usuarios buscar, administrar y organizar la cantidad creciente de datos comunes en entornos empresariales y domésticos.<br/>                                                                                                                                                                                    |
| [Estaciones de ventana y equipos de escritorio](./winstation/window-stations-and-desktops.md)<br/> | Windows proporciona tres categorías principales de objetos: interfaz de usuario, interfaz de dispositivo gráfico (GDI) y kernel. Los objetos de kernel son protegibles, mientras que los objetos de usuario y los objetos GDI no lo son. Por lo tanto, para proporcionar seguridad adicional, los objetos de interfaz de usuario se administran mediante estaciones de ventana y equipos de escritorio, que a su vez son objetos protegibles.<br/>                                                                                                                                                                                                                                              |
| [Ayuda de Windows](/windows/win32/api/winuser/nf-winuser-winhelpa)<br/>                                        | Describe las tecnologías de ayuda disponibles en Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [Consolas](/windows/console/character-mode-applications)<br/>                        | Las consolas de administran la entrada y salida (e/s) para aplicaciones en modo de caracteres (aplicaciones que no proporcionan su propia interfaz gráfica de usuario).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de la interfaz de usuario de aplicaciones Windows](./windows-application-ui-development.md)
</dt> </dl>

 

 
