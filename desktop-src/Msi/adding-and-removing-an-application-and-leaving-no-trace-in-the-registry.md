---
description: Si se debe registrar una aplicación, cree el paquete de instalación como se describe en la sección Agregar y quitar claves del Registro en la instalación o eliminación de componentes.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Agregar y quitar una aplicación y no dejar ningún seguimiento en el Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36804633a51e0e2f4beafc37e9f830e1743a5ac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159218"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Agregar y quitar una aplicación y no dejar ningún seguimiento en el Registro

Si se debe registrar una aplicación, cree el paquete de instalación como se describe en la sección Agregar y quitar claves del Registro en la instalación o eliminación [de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). El instalador usa el registro para anuncios y la característica Agregar o quitar programas de Panel de control. Si una aplicación no está registrada, no se puede anunciar y no aparece en la característica Agregar o quitar programas de Panel de control.

Puede omitir el registro de una aplicación quitando las acciones [RegisterProduct](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md)y [PublishFeatures](publishfeatures-action.md) de las tablas [InstallExecuteSequence](installexecutesequence-table.md) y [AdvtExecuteSequence](advtexecutesequence-table.md). Todas estas acciones deben quitarse o algún seguimiento de la aplicación puede permanecer en el Registro. Al quitar todas estas acciones, se impide que la aplicación aparezca en la característica Agregar o quitar programas de Panel de control y se impide el anuncio de la aplicación. La eliminación de todas estas acciones también impide que la aplicación se registre con los datos de configuración Windows Installer. Esto significa que no puede quitar, reparar ni reinstalar [](command-line-options.md)la aplicación mediante las opciones de la línea de comandos del instalador de Windows o la interfaz de programación de aplicaciones (API) del instalador de Windows.

Para ocultar una aplicación de la característica Agregar o quitar programas de Panel de control y poder seguir utilizando el Instalador de Windows para administrar una aplicación, [](property-table.md) deje las acciones de registro en las tablas de secuencia y establezca la propiedad [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) de la tabla de propiedades en 1 (una). La aplicación no aparece en la característica Agregar o quitar programas, pero puede usar el instalador de Windows para instalar a petición, desinstalar, reparar y reinstalar la aplicación.

 

 



