---
description: En WMI, una clase es un objeto que describe algún aspecto de una empresa, como un tipo especial de unidad de disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Crear una clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678343"
---
# <a name="creating-a-wmi-class"></a>Crear una clase WMI

En WMI, una clase es un objeto que describe algún aspecto de una empresa, como un tipo especial de unidad de disco. Después de crear una definición de clase, escriba la DLL del proveedor para proporcionar instancias de la clase, los datos de propiedad y los métodos de ejecución definidos para la clase. Los scripts y las aplicaciones pueden obtener datos o controlar el dispositivo. Para obtener más información, vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).

> [!Note]  
> Para asegurarse de que todas las definiciones de clases de WMI para objetos administrados se restauran en el [*repositorio de WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador de la instrucción [**\# pragma AUTORECOVER**](pragma-autorecover.md) en el archivo MOF.

 

## <a name="base-class"></a>Clase base

Una clase base representa un concepto general. Por ejemplo, la clase [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) representa todos los tipos de unidades de CD-ROM en WMI y contiene propiedades generales que describen todos los tipos de unidades de CD-ROM. Para obtener más información, vea [crear una clase base](creating-a-base-class.md).

Una clase derivada hereda propiedades y métodos de otra clase. Normalmente, una clase derivada representa un caso específico de una clase base. Por ejemplo, la [**clase \_ CDROMDrive de Win32**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) representa una unidad de CD-ROM en un sistema Windows. La **clase \_ CDROMDrive de Win32** se basa en y hereda muchas de las propiedades de [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive). Sin embargo, **Win32 \_ CDROMDrive**, al igual que otras clases derivadas, pueden tener propiedades adicionales que hacen que la clase derivada sea única. Para obtener más información, vea [crear una clase derivada](creating-a-derived-class.md).

## <a name="properties-and-methods"></a>Propiedades y métodos

Crear una clase significa definir las propiedades que describen esa clase. También puede definir métodos que manipulen el objeto representado por la clase.

Por lo general, una propiedad representa un aspecto del objeto, como un número de serie para un dispositivo o un tamaño en bytes para un proceso, mientras que un método representa una acción que cambia el estado o el comportamiento del dispositivo o de la entidad lógica.

Cada clase debe tener al menos una propiedad de clave. Aunque una clase puede tener varias claves, no se puede crear una instancia de una clase con más de 256 claves.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases de Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
