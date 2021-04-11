---
description: Para instalar un archivo, una fuente o una clave del registro para que no se quite cuando se desinstale el producto, el componente completo que contiene el archivo, la fuente o la clave del registro debe ser permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalación de componentes permanentes, archivos, fuentes y claves del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083444"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Instalación de componentes permanentes, archivos, fuentes y claves del registro

Para instalar un archivo, una fuente o una clave del registro para que no se quite cuando se desinstale el producto, el componente completo que contiene el archivo, la fuente o la clave del registro debe ser permanente. Para que un componente sea permanente, establezca **msidbComponentAttributesPermanent** en la columna Attributes de la [tabla Component](component-table.md).

Tenga en cuenta que el instalador quita una clave del registro después de quitar el último valor o subclave de la clave. Para evitar que se quite una clave del Registro vacía al desinstalar, escriba un valor ficticio en la clave que necesita conservar y escriba + en la columna Nombre de la [tabla del registro](registry-table.md).

 

 



