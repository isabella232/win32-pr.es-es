---
description: Instrumental de administración de Windows (WMI) define un conjunto de propiedades del sistema que se asocian a todas las clases e instancias de clases.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propiedades del sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276247"
---
# <a name="wmi-system-properties"></a>Propiedades del sistema WMI

Instrumental de administración de Windows (WMI) define un conjunto de propiedades del sistema que se asocian a todas las clases e instancias de clases. Al igual que con las clases del sistema, los nombres de propiedad del sistema comienzan con un carácter de subrayado doble, para distinguirlos de las propiedades creadas por aplicaciones o proveedores que no deben comenzar por un carácter de subrayado simple o doble. Otra manera de identificar una propiedad del sistema es usar el método [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

Las propiedades del sistema están disponibles en cualquier momento, pero los valores pueden ser **null**. **Null** indica que una propiedad no se aplica a un objeto concreto. Sin embargo, es posible que las propiedades del sistema no estén disponibles en todo momento para todas las clases o instancias.

## <a name="system-properties"></a>Propiedades del sistema

En la lista siguiente se describen las propiedades del sistema WMI. Los ejemplos proporcionados se toman de las propiedades del sistema de la clase [**\_ OptionalFeature de Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que se describe en la parte inferior de este tema.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Las**
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura para instancias; lectura/escritura para clases

Nombre de la clase.

Ejemplo: Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Deriva**
</dt> <dd>

Tipo de datos: matriz de **\_ cadenas CIM**

Tipo de acceso: solo lectura para instancias y clases

Jerarquía de clases de la clase o instancia actual. El primer elemento es la clase primaria inmediata, el siguiente es su elemento primario, y así sucesivamente; el último elemento es la clase base.

Ejemplo: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura

Nombre de la clase de nivel superior de la que se deriva la clase o la instancia. Cuando esta clase o instancia es la clase de nivel superior, los valores de **\_ \_ Dynasty** y **\_ \_ Class** son los mismos.

Ejemplo: el \_ ManagedSystemElement de CIM

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Género**
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Tipo de acceso: solo lectura

Valor que se usa para distinguir entre clases e instancias. Este valor es **la \_ \_ clase de género de WBEM** (1) para las clases y la **\_ \_ instancia de género de WBEM** (2) para instancias y eventos.

Ejemplo: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_System.IO**](--namespace.md)
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura

Nombre del [*espacio de nombres*](gloss-n.md) de la clase o la instancia.

Ejemplo: raíz \\ cimv2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Camino**
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura

Ruta de acceso completa a la clase o instancia, incluido el servidor y el espacio de nombres.

Ejemplo: \\ \\ servidor \\ raíz \\ cimv2: Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Recuento de propiedades \_**
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Tipo de acceso: solo lectura

Número de propiedades no del sistema definidas para la clase o la instancia.

Ejemplo: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura

Ruta de acceso relativa a la clase o instancia.

Ejemplo: Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servidor**
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura

Nombre del servidor que proporciona la clase o la instancia.

Ejemplo: mi Server

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Dados**
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Tipo de acceso: solo lectura

Nombre de la clase primaria inmediata de la clase o instancia.

Ejemplo: CIM \_ LogicalElement

</dd> </dl>

El siguiente código de PowerShell recupera las propiedades de la [**clase \_ OptionalFeature de Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que incluye las propiedades del sistema.


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



El ejemplo de código anterior devuelve lo siguiente:


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
