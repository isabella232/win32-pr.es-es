---
title: Windows Marco de la cinta de opciones
description: Lea una introducción al marco Windows Ribbon, que es una alternativa moderna a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows Cinta
- Cinta de opciones
- Windows Documentación de la cinta de opciones
- Documentación de la cinta de opciones
- Windows API de cinta
- API de cinta
- Windows Ribbon,framework
- Ribbon,framework
- Windows Cinta de opciones, acerca de
- Cinta de opciones, acerca de
- Windows Cinta de opciones, componentes
- Cinta de opciones, componentes
- Windows Cinta de opciones, vistas
- Cinta de opciones, vistas
- Windows Cinta de opciones, arquitectura
- Cinta de opciones, arquitectura
- Windows Cinta de opciones, API
- Cinta de opciones, API
- Windows Cinta de opciones, seguridad
- Cinta de opciones, seguridad
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 98f7dbf42d604f93c76bb9897aa25918d45d126f
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691654"
---
# <a name="windows-ribbon-framework"></a>Windows Marco de la cinta de opciones

El marco Windows ribbon es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales. Similar en funcionalidad y apariencia a la interfaz de usuario de Microsoft Office 2007 Fluent, el marco de la cinta de opciones se compone de una barra de comandos de la cinta de opciones que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación y un sistema de menú contextual.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                           | Descripción                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre el marco de opciones](windowsribbon-overviews-entry.md)<br/>      | Los temas contenidos en esta sección exploran los aspectos básicos del marco de la cinta de opciones. <br/>                                                                                                                   |
| [Guías para desarrolladores de Ribbon Framework](windowsribbon-guides-entry.md)<br/>  | Los temas contenidos en esta sección describen aspectos específicos del marco Windows Ribbon. <br/>                                                                                                          |
| [Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)<br/> | Los temas contenidos en esta sección describen el conjunto de controles que se incluyen con el marco de la cinta de opciones. Los controles enumerados aquí son los objetos de interfaz de usuario de una cinta de opciones que exponen la funcionalidad Command.<br/> |
| [Referencia del marco de opciones](windowsribbon-reference-entry.md)<br/>      | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para el marco de la cinta de opciones.<br/>                                                                                                       |
| [Ejemplos del marco de opciones](windowsribbon-samples-entry.md)<br/>          | Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del marco Windows Ribbon. <br/>                                                                     |
| [Glosario del marco de opciones](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Audiencia de los desarrolladores

El marco Windows ribbon está diseñado para su uso por desarrolladores de C/C++ y diseñadores de interfaz de usuario.

Ventajas recomendadas:

- Programación COM
- Windows Programación de API
- Programación XML/XAML

Conocimientos básicos recomendados:

- Conceptos de programación de la interfaz de usuario
- Conceptos generales de la interfaz de usuario

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible               | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) y [Platform Update para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo compatible               | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 y [Platform Update para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de desarrollo de software de Windows (SDK) | 7.0                                                                                                                                                                      |
| Archivos de encabezado e IDL                   | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de la cinta de opciones Windows a Windows Vista y Windows Server 2008. Las actualizaciones de la plataforma estarán disponibles para todos los Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden hacer que Windows Update detecte si está instalada la actualización necesaria; Si no es así, Windows Update la descargará e instalará en segundo plano.

 

## <a name="see-also"></a>Consulte también

[Modelo de objetos componentes (COM)](../com/component-object-model--com--portal.md)


[API de Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

