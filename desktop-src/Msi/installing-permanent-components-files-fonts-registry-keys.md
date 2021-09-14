---
description: Para instalar un archivo, una fuente o una clave del Registro para que no se quite cuando se desinstale el producto, todo el componente que contiene el archivo, la fuente o la clave del Registro debe ser permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalación de componentes permanentes, archivos, fuentes y claves del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072041"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Instalación de componentes permanentes, archivos, fuentes y claves del Registro

Para instalar un archivo, una fuente o una clave del Registro para que no se quite cuando se desinstale el producto, todo el componente que contiene el archivo, la fuente o la clave del Registro debe ser permanente. Para que un componente sea permanente, **establezca msidbComponentAttributesPermanent en** la columna Atributos de la [tabla Component](component-table.md).

Tenga en cuenta que el instalador quita una clave del Registro después de quitar el último valor o subclave bajo la clave. Para evitar que se quite una clave del Registro vacía en la desinstalación, escriba un valor ficticio en la clave que necesita conservar y escriba + en la columna Nombre de la [tabla del Registro](registry-table.md).

 

 



