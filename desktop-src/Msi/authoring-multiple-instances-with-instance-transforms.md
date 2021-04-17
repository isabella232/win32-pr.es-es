---
description: Para instalar varias instancias de un producto de un paquete de Windows Installer, debe crear un paquete de instalación base para el producto y una transformación de instancia para cada instancia que se va a instalar además de la instancia base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Crear varias instancias con transformaciones de instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667030"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Crear varias instancias con transformaciones de instancia

Para instalar varias instancias de un producto de un paquete de Windows Installer, debe crear un paquete de instalación base para el producto y una transformación de instancia para cada instancia que se va a instalar además de la instancia base. Use las siguientes directrices al crear el paquete base y las transformaciones:

-   La aplicación de instalación puede comprobar la presencia del instalador que se ejecuta en una versión de Windows Vista, Windows Server 2003, Windows XP con Service Pack 1 (SP1) y el Windows Installer 3,0 Redistributable. Cualquiera de estas versiones del instalador (o posterior) son necesarias para instalar varias instancias de un único paquete con un código de producto: cambio de transformación.
-   Cada instancia debe tener un código de producto y un identificador de instancia únicos. Puede definir una propiedad en el paquete base, cuyo valor se puede establecer en el identificador de la instancia.
-   Para mantener aislados los archivos de cada instancia, el paquete base debe instalar los archivos en una ubicación de directorio que dependa del identificador de la instancia.
-   Para mantener aislados los datos que no son de archivo de cada instancia, el paquete base debe recopilar datos que no son de archivo en conjuntos de componentes para cada instancia. Los componentes adecuados deben instalarse en función de las instrucciones condicionales que dependen del identificador de la instancia.
-   Cree una transformación de instancia para cada instancia que se está instalando además de la instancia base. El paquete base puede instalar su propia instancia.
-   La transformación de la instancia debe cambiar el código de producto y el identificador de cada instancia.
-   Se recomienda que la transformación del producto cambie también el nombre del producto para que la instancia sea más fácil de distinguir en Agregar o quitar programas a través del panel de control.
-   Si la transformación de instancia instala archivos, deben instalarse en un directorio que dependa del identificador de la instancia.
-   Todos los datos que no son de archivo, como las claves del registro, deben incluir el nombre de instancia en su ruta de acceso para evitar colisiones. Esto puede realizarse mediante el uso de la propiedad cuyo valor es el identificador de instancia en la ruta de acceso, tal como se muestra en el siguiente ejemplo de una [tabla del registro](registry-table.md).



| Registro | Root | Clave                                            | Nombre         | Value           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft el \\ \\ \[ InstanceId\] | Valor FileStream | \[ProductCode\] | NonFileDataComp1 |



 

Para obtener más información, vea [instalar varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md) e [instalar varias instancias con transformaciones de instancias](installing-multiple-instances-with-instance-transforms.md).

 

 



