---
description: Para instalar varias instancias de un producto desde un paquete de Windows Installer, debe crear un paquete de instalación base para el producto y una transformación de instancia para cada instancia que se va a instalar además de la instancia base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Creación de varias instancias con transformaciones de instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efac957d5e0e82665cb1ba20aeb42fe9b60293699c5c3fd97f5e6a6f1abf58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745915"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Creación de varias instancias con transformaciones de instancia

Para instalar varias instancias de un producto desde un paquete de Windows Installer, debe crear un paquete de instalación base para el producto y una transformación de instancia para cada instancia que se va a instalar además de la instancia base. Use las siguientes directrices al crear el paquete base y las transformaciones:

-   La aplicación de instalación puede comprobar la presencia del instalador que se ejecuta en una versión de Windows Vista, Windows Server 2003, Windows XP con Service Pack 1 (SP1) y el instalador de Windows 3.0 redistribuible. Cualquiera de estas versiones del instalador (o posterior) es necesaria para instalar varias instancias desde un único paquete mediante una transformación de cambio de código de producto.
-   Cada instancia debe tener un código de producto único y un identificador de instancia. Puede definir una propiedad en el paquete base, cuyo valor se puede establecer en el identificador de instancia.
-   Para mantener aislados los archivos de cada instancia, el paquete base debe instalar los archivos en una ubicación de directorio que dependa del identificador de instancia.
-   Para mantener aislados los datos que no son de archivo de cada instancia, el paquete base debe recopilar datos que no son de archivo en conjuntos de componentes para cada instancia. A continuación, se deben instalar los componentes adecuados en función de las instrucciones condicionales que dependen del identificador de instancia.
-   Cree una transformación de instancia para cada instancia que se va a instalar además de la instancia base. El paquete base puede instalar su propia instancia.
-   La transformación de instancia debe cambiar el código de producto y el identificador de cada instancia.
-   Se recomienda que la transformación del producto también cambie el nombre del producto para que la instancia se distinga fácilmente en Agregar o quitar programas a través de Panel de control.
-   Si la transformación de instancia instala archivos, deben instalarse en un directorio que dependa del identificador de instancia.
-   Todos los datos que no son de archivos, como las claves del Registro, deben incluir el nombre de instancia en su ruta de acceso para evitar colisiones. Esto se puede lograr mediante la propiedad cuyo valor es el identificador de instancia en la ruta de acceso, como se muestra en el ejemplo siguiente de una tabla [del Registro](registry-table.md).



| Registro | Root | Clave                                            | Nombre         | Value           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Id. \\ de instancia de Microsoft \\ MyProduct de \\ \[ software\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Para obtener más información, vea Instalar varias instancias de [productos y revisiones](installing-multiple-instances-of-products-and-patches.md) e Instalar varias instancias con [transformaciones de instancia.](installing-multiple-instances-with-instance-transforms.md)

 

 



