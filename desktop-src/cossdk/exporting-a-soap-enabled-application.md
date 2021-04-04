---
description: Cuando se utiliza COM+ para crear un servicio Web XML, el servicio puede ser utilizado por cualquier cliente autorizado, incluidos los que no usan COM+ ni siquiera Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportar una aplicación SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907352"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportar una aplicación SOAP-Enabled

Cuando se utiliza COM+ para crear un servicio Web XML, el servicio puede ser utilizado por cualquier cliente autorizado, incluidos los que no usan COM+ ni siquiera Microsoft Windows. Sin embargo, el uso de un servicio Web COM+ en el modo de objetos activados en el cliente (CAO) desde una aplicación cliente COM+ es especialmente fácil. Simplemente exporte la aplicación habilitada para SOAP en modo proxy y, a continuación, [impórtela](importing-a-soap-enabled-application.md) en el cliente para el que desea obtener acceso al servicio Web XML correspondiente.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para exportar una aplicación habilitada para SOAP desde un servidor, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.

2.  Haga clic con el botón secundario en el componente que desee exponer como un servicio Web XML y elija **exportar**. Aparece el **Asistente para la exportación de aplicaciones com+** .

3.  En el cuadro de texto con la etiqueta **Escriba la ruta de acceso completa y el nombre del archivo de la aplicación que se va a crear**, escriba la ruta de acceso completa y el nombre del archivo MSI que contendrá la aplicación exportada, o haga clic en **examinar** para seleccionar la ruta de acceso completa y el nombre de archivo mediante un cuadro de diálogo.

4.  En **exportar como**, seleccione el botón de radio **aplicación proxy: instalar en otros equipos para habilitar el acceso a este equipo** .

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción al servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Crear servicios Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importar una aplicación SOAP-Enabled](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



