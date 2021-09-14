---
description: Para instalar varias instancias de un producto desde un paquete del instalador de Windows, debe crear un paquete de instalación base para el producto y una transformación de instancia para cada instancia que se va a instalar además de la instancia base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Creación de varias instancias con transformaciones de instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159025"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Creación de varias instancias con transformaciones de instancia

Para instalar varias instancias de un producto desde un paquete del instalador de Windows, debe crear un paquete de instalación base para el producto y una transformación de instancia para cada instancia que se va a instalar además de la instancia base. Use las siguientes directrices al crear el paquete base y las transformaciones:

-   La aplicación de instalación puede comprobar la presencia del instalador que se ejecuta en una versión de Windows Vista, Windows Server 2003, Windows XP con Service Pack 1 (SP1) y el instalador de Windows 3.0 redistribuible. Cualquiera de estas versiones del instalador (o posterior) es necesaria para instalar varias instancias de un único paquete mediante una transformación de cambio de código de producto.
-   Cada instancia debe tener un código de producto único y un identificador de instancia. Puede definir una propiedad en el paquete base, cuyo valor se puede establecer en el identificador de instancia.
-   Para mantener aislados los archivos de cada instancia, el paquete base debe instalar los archivos en una ubicación de directorio que dependa del identificador de instancia.
-   Para mantener aislados los datos que no son de archivo de cada instancia, el paquete base debe recopilar datos que no son de archivo en conjuntos de componentes para cada instancia. A continuación, se deben instalar los componentes adecuados en función de instrucciones condicionales que dependan del identificador de instancia.
-   Cree una transformación de instancia para cada instancia que se va a instalar además de la instancia base. El paquete base puede instalar su propia instancia.
-   La transformación de instancia debe cambiar el código de producto y el identificador de cada instancia.
-   Se recomienda que la transformación del producto también cambie el nombre del producto para que la instancia se distinga fácilmente en Agregar o quitar programas mediante Panel de control.
-   Si la transformación de instancia instala archivos, deben instalarse en un directorio que dependa del identificador de instancia.
-   Todos los datos que no son de archivo, como las claves del Registro, deben incluir el nombre de instancia en su ruta de acceso para evitar colisiones. Esto se puede lograr mediante la propiedad cuyo valor es el identificador de instancia en la ruta de acceso, como se muestra en el ejemplo siguiente de una tabla [del Registro](registry-table.md).



| Registro | Root | Clave                                            | Nombre         | Value           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Id. \\ de instancia de Microsoft \\ MyProduct de \\ \[ software\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Para obtener más información, vea [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) (Instalación de varias instancias de productos y revisiones) e [Installing Multiple Instances with Instance Transforms](installing-multiple-instances-with-instance-transforms.md)(Instalación de varias instancias con transformaciones de instancia).

 

 



