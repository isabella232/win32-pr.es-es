---
description: Windows Instrumental de administración (WMI) define un conjunto de propiedades del sistema que están asociadas a todas las clases e instancias de clases.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propiedades del sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3471665e2e818037bb831c8d8ab39bbe0d56e01912afb1a3399b4055d3670a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120665"
---
# <a name="wmi-system-properties"></a>Propiedades del sistema WMI

Windows Instrumental de administración (WMI) define un conjunto de propiedades del sistema que están asociadas a todas las clases e instancias de clases. Al igual que con las clases del sistema, los nombres de propiedad del sistema comienzan con un carácter de subrayado doble, distinguiendolos de las propiedades creadas por aplicaciones o proveedores que no deben comenzar con un carácter de subrayado único o doble. Otra manera de identificar una propiedad del sistema es usar el [**método IWbemClassObject::Get.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

Las propiedades del sistema están disponibles en cualquier momento, pero los valores pueden ser **NULL.** **NULL** indica que una propiedad no se aplica a un objeto específico. Sin embargo, es posible que las propiedades del sistema no estén disponibles todo el tiempo para todas las clases o instancias.

## <a name="system-properties"></a>Propiedades del sistema

En la lista siguiente se describen las propiedades del sistema WMI. Los ejemplos que se proporcionan se toman de las propiedades del sistema de la clase [**\_ OptionalFeature de Win32,**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) que se describe en la parte inferior de este tema.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Clase**
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura para instancias; lectura y escritura para clases

Nombre de la clase.

Ejemplo: Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivación**
</dt> <dd>

Tipo de datos: **matriz \_ CIM STRING**

Tipo de acceso: solo lectura para instancias y clases

Jerarquía de clases de la clase o instancia actual. El primer elemento es la clase primaria inmediata, el siguiente es su elemento primario, y así sucesivamente; El último elemento es la clase base.

Ejemplo: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dinastía**
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura

Nombre de la clase de nivel superior de la que se deriva la clase o instancia. Cuando esta clase o instancia es la clase de nivel superior, los valores **\_ \_ de Tiempo** y **\_ \_ Clase** son los mismos.

Ejemplo: CIM \_ ManagedSystemElement

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Género**
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Tipo de acceso: solo lectura

Valor que se usa para distinguir entre clases e instancias. Este valor es **WBEM \_ UNA CLASE DE INSERTE \_** (1) para las clases y **WBEM UNA INSTANCIA DE \_ ESTA \_** (2) para instancias y eventos.

Ejemplo: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Nombres**](--namespace.md)
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura

Nombre del espacio [*de nombres*](gloss-n.md) de la clase o instancia.

Ejemplo: root \\ cimv2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Camino**
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura

Ruta de acceso completa a la clase o instancia, incluidos el servidor y el espacio de nombres.

Ejemplo: \\ \\ Raíz de MyServer \\ \\ cimv2:Win32 \_ OptionalFeature.Name="TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Recuento de \_ propiedades**
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Tipo de acceso: solo lectura

Número de propiedades no del sistema definidas para la clase o instancia.

Ejemplo: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura

Ruta de acceso relativa a la clase o instancia.

Ejemplo: Win32 \_ OptionalFeature.Name="TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servidor**
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura

Nombre del servidor que proporciona la clase o instancia.

Ejemplo: MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclase**
</dt> <dd>

Tipo de datos: **CIM \_ STRING**

Tipo de acceso: solo lectura

Nombre de la clase primaria inmediata de la clase o instancia.

Ejemplo: Cim \_ LogicalElement

</dd> </dl>

El siguiente código de PowerShell recupera las propiedades de la clase [**\_ OptionalFeature de Win32,**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) que incluye las propiedades del sistema.


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



 

 
