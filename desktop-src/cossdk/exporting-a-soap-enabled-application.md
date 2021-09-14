---
description: Cuando se usa COM+ para crear un servicio web XML, cualquier cliente autorizado puede usar ese servicio, incluidos aquellos que no usan COM+ o incluso Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportación de una SOAP-Enabled aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160498"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportación de una SOAP-Enabled aplicación

Cuando se usa COM+ para crear un servicio web XML, cualquier cliente autorizado puede usar ese servicio, incluidos aquellos que no usan COM+ o incluso Microsoft Windows. Sin embargo, el uso de un servicio web COM+ en modo de objeto activado por el cliente (DHCP) desde una aplicación cliente COM+ es especialmente fácil. Solo tiene que exportar la aplicación habilitada [](importing-a-soap-enabled-application.md) para SOAP en modo proxy y, a continuación, importarla en el cliente para el que desea acceder al servicio web XML correspondiente.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para exportar una aplicación habilitada para SOAP desde un servidor, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en Servicios de componentes **,** abra la carpeta **Aplicaciones COM+** asociada al equipo que desea administrar.

2.  Haga clic con el botón derecho en el componente que desea exponer como servicio web XML y elija **Exportar.** Aparece **el Asistente para exportación de aplicaciones COM+.**

3.  En el cuadro de texto con la etiqueta Escriba la ruta de acceso completa y el nombre de archivo del  archivo de aplicación que se va a **crear,** escriba la ruta de acceso completa y el nombre de archivo del archivo MSI que contendrá la aplicación exportada o haga clic en Examinar para seleccionar la ruta de acceso completa y el nombre de archivo mediante un cuadro de diálogo.

4.  En **Exportar como**, seleccione el botón de radio Application Proxy – Instalar en **otras** máquinas para habilitar el acceso a esta máquina.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Creación de servicios Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importación de una SOAP-Enabled aplicación](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



