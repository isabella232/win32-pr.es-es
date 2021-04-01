---
title: Marco de cinta de Windows
description: El marco de la cinta de opciones de Windows es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Cinta de Windows
- Cinta de opciones
- Documentación de la cinta de Windows
- Documentación de la cinta
- API de la cinta de opciones de Windows
- API de la cinta
- Cinta de Windows, marco
- Cinta de opciones, marco
- Cinta de Windows, acerca de
- Cinta, acerca de
- Cinta de Windows, componentes
- Cinta de opciones, componentes
- Cinta de opciones de Windows, vistas
- Cinta de opciones, vistas
- Cinta de Windows, arquitectura
- Cinta de opciones, arquitectura
- Cinta de Windows, API
- Cinta de opciones, API
- Cinta de opciones de Windows, seguridad
- Cinta de opciones, seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6906401573cb244ddc4386faf8c283d7938a0ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996239"
---
# <a name="windows-ribbon-framework"></a>Marco de cinta de Windows

El marco de la cinta de opciones de Windows es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales. Similar en cuanto a la funcionalidad y la apariencia de la interfaz de usuario fluida de Microsoft Office 2007, el marco de la cinta de opciones se compone de una barra de comandos de la cinta de opciones que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación y un sistema de menús contextuales.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                           | Descripción                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general del marco de cinta](windowsribbon-overviews-entry.md)<br/>      | Los temas contenidos en esta sección exploran los aspectos básicos del marco de la cinta de opciones. <br/>                                                                                                                   |
| [Guías para desarrolladores del marco de cinta](windowsribbon-guides-entry.md)<br/>  | Los temas incluidos en esta sección describen aspectos específicos del marco de la cinta de opciones de Windows. <br/>                                                                                                          |
| [Biblioteca de controles del marco de cinta](windowsribbon-controls-entry.md)<br/> | En los temas incluidos en esta sección se describe el conjunto de controles que se incluyen con el marco de la cinta de opciones. Los controles que se muestran aquí son los objetos de interfaz de usuario de una cinta que exponen la funcionalidad del comando.<br/> |
| [Referencia del marco de cinta](windowsribbon-reference-entry.md)<br/>      | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para el marco de cinta.<br/>                                                                                                       |
| [Ejemplos de marcos de cinta](windowsribbon-samples-entry.md)<br/>          | Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del marco de la cinta de opciones de Windows. <br/>                                                                     |
| [Glosario de marcos de cinta](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Audiencia de los desarrolladores

El marco de la cinta de Windows está diseñado para que lo usen los desarrolladores de C/C++ y los diseñadores de la interfaz de usuario.

Proficiencies recomendado:

-   Programación COM
-   Programación de la API de Windows
-   Programación XML/XAML

Conocimientos fundamentales recomendados:

-   Conceptos de programación de la interfaz de usuario
-   Conceptos generales de la interfaz de usuario

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Value |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible               | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) y la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo compatible               | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 y [actualización de la plataforma para Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de desarrollo de software de Windows (SDK) | 7.0                                                                                                                                                                      |
| Archivos de encabezado y IDL                   | uiribbon. h, uiribbon. idl                                                                                                                                                 |



 

> [!Note]  
> La [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores tener como destino aplicaciones de cinta de Windows para Windows Vista y Windows Server 2008. Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.

 

## <a name="see-also"></a>Consulte también

[Modelo de objetos componentes (COM)](../com/component-object-model--com--portal.md)


[API de Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

