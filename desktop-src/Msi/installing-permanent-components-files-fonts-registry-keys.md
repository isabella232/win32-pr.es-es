---
description: Para instalar un archivo, una fuente o una clave del Registro para que no se quite cuando se desinstale el producto, todo el componente que contiene el archivo, la fuente o la clave del Registro debe ser permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalación de componentes permanentes, archivos, fuentes y claves del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87818c2b9a80d582992dd964daa632575f51e5fa24f17a97af0191277e880df6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105105"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Instalación de componentes permanentes, archivos, fuentes y claves del Registro

Para instalar un archivo, una fuente o una clave del Registro para que no se quite cuando se desinstale el producto, todo el componente que contiene el archivo, la fuente o la clave del Registro debe ser permanente. Para que un componente sea permanente, **establezca msidbComponentAttributesPermanent en** la columna Atributos de la [tabla Component](component-table.md).

Tenga en cuenta que el instalador quita una clave del Registro después de quitar el último valor o subclave bajo la clave. Para evitar que se quite una clave del Registro vacía en la desinstalación, escriba un valor ficticio en la clave que necesita conservar y escriba + en la columna Nombre de la [tabla del Registro](registry-table.md).

 

 



