---
title: Marco de la cinta de opciones de Windows
description: Lea una introducción al marco de la cinta de opciones de Windows, que es una alternativa moderna a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones tradicionales de Windows.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Cinta de opciones de Windows
- Cinta de opciones
- Documentación de la cinta de opciones de Windows
- Documentación de la cinta de opciones
- API de la cinta de opciones de Windows
- API de cinta
- Cinta de opciones de Windows, marco
- Ribbon,framework
- Cinta de opciones de Windows, acerca de
- Cinta de opciones, acerca de
- Cinta de opciones de Windows, componentes
- Cinta de opciones, componentes
- Cinta de opciones de Windows, vistas
- Cinta de opciones, vistas
- Cinta de opciones de Windows, arquitectura
- Cinta de opciones, arquitectura
- Cinta de opciones de Windows, API
- Cinta de opciones, API
- Cinta de opciones de Windows, seguridad
- Cinta de opciones, seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211e1e1cf39a547ad0edbc0c180c62e2f40e15fa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406368"
---
# <a name="windows-ribbon-framework"></a>Marco de la cinta de opciones de Windows

El marco de la cinta de opciones de Windows es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones tradicionales de Windows. Similar en funcionalidad y apariencia a la interfaz de usuario fluent de Microsoft Office 2007, el marco de la cinta de opciones se compone de una barra de comandos de cinta de opciones que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación y un sistema de menús contextuales.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                           | Descripción                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre el marco de opciones](windowsribbon-overviews-entry.md)<br/>      | Los temas contenidos en esta sección exploran los aspectos básicos del marco de la cinta de opciones. <br/>                                                                                                                   |
| [Guías para desarrolladores de Ribbon Framework](windowsribbon-guides-entry.md)<br/>  | Los temas contenidos en esta sección describen aspectos específicos del marco de la cinta de opciones de Windows. <br/>                                                                                                          |
| [Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)<br/> | Los temas contenidos en esta sección describen el conjunto de controles que se incluyen con el marco de la cinta de opciones. Los controles enumerados aquí son los objetos de interfaz de usuario de una cinta de opciones que exponen la funcionalidad Command.<br/> |
| [Referencia del marco de opciones](windowsribbon-reference-entry.md)<br/>      | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para el marco de la cinta de opciones.<br/>                                                                                                       |
| [Ejemplos del marco de opciones](windowsribbon-samples-entry.md)<br/>          | Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del marco de la cinta de opciones de Windows. <br/>                                                                     |
| [Glosario del marco de opciones](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Audiencia de los desarrolladores

El marco de la cinta de opciones de Windows está diseñado para su uso por desarrolladores de C/C++ y diseñadores de interfaz de usuario.

Ventajas recomendadas:

-   Programación COM
-   Programación de API de Windows
-   Programación XML/XAML

Conocimientos básicos recomendados:

-   Conceptos de programación de la interfaz de usuario
-   Conceptos generales de la interfaz de usuario

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible               | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) y [actualización de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo compatible               | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 y [actualización de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de desarrollo de software de Windows (SDK) | 7.0                                                                                                                                                                      |
| Archivos de encabezado e IDL                   | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de la cinta de opciones de Windows a Windows Vista y Windows Server 2008. Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden Windows Update detectar si está instalada la actualización necesaria; Si no es así, Windows Update descargará e instalará en segundo plano.

 

## <a name="see-also"></a>Consulte también

[Modelo de objetos componentes (COM)](../com/component-object-model--com--portal.md)


[API de Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

