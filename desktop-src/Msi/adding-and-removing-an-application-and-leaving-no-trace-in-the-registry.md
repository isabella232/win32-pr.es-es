---
description: Si se debe registrar una aplicación, cree el paquete de instalación como se describe en la sección agregar y quitar claves del registro en la instalación o desinstalación de componentes.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36804633a51e0e2f4beafc37e9f830e1743a5ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001761"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro

Si se debe registrar una aplicación, cree el paquete de instalación como se describe en la sección [Agregar y quitar claves del registro en la instalación o desinstalación de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). El instalador usa el registro para el anuncio y la característica agregar o quitar programas del panel de control. Si una aplicación no está registrada, no se puede anunciar y no aparece en la característica agregar o quitar programas del panel de control.

Puede omitir el registro de una aplicación mediante la eliminación de la acción [RegisterProduct](registerproduct-action.md), la acción [RegisterUser](registeruser-action.md), la [acción PublishProduct](publishproduct-action.md)y la [acción PublishFeatures](publishfeatures-action.md) de la [tabla InstallExecuteSequence](installexecutesequence-table.md) y la [tabla AdvtExecuteSequence](advtexecutesequence-table.md). Todas estas acciones deben quitarse, o puede que algún seguimiento de la aplicación permanezca en el registro. La eliminación de todas estas acciones evita que la aplicación se muestre en la característica agregar o quitar programas del panel de control y evita el anuncio de la aplicación. La eliminación de todas estas acciones también evita que la aplicación se registre con los datos de configuración Windows Installer. Esto significa que no se puede quitar, reparar ni volver a instalar la aplicación mediante el uso de las [Opciones de línea de comandos](command-line-options.md)de Windows Installer o la interfaz de programación de aplicaciones (API) de Windows Installer.

Para ocultar una aplicación de la característica agregar o quitar programas del panel de control y seguir pudiendo usar el Windows Installer para administrar una aplicación, deje las acciones de registro en las tablas de secuencia y establezca la [**propiedad ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) de la [tabla de propiedades](property-table.md) en 1 (uno). La aplicación no aparece en la característica agregar o quitar programas, pero puede usar la Windows Installer para instalarla a petición, desinstalar, reparar y volver a instalar la aplicación.

 

 



