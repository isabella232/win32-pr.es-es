---
description: De forma predeterminada, una aplicación o script recibe datos del proveedor correspondiente cuando existen dos versiones de proveedores.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Solicitud de datos WMI en una plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063924"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Solicitud de datos WMI en una plataforma de 64 bits

De forma predeterminada, una aplicación o script recibe datos del proveedor correspondiente cuando existen dos versiones de proveedores. El proveedor de 32 bits devuelve datos a una aplicación de 32 bits, incluidos todos los scripts, y el proveedor de 64 bits devuelve datos a las aplicaciones compiladas de 64 bits. Sin embargo, una aplicación o script puede solicitar datos del proveedor no predeterminado, si existe, notificando a WMI a través de marcas en llamadas a métodos.

## <a name="context-flags"></a>Marcas de contexto

Las marcas de cadena **\_ \_ ProviderArchitecture** y **\_ \_ RequiredArchitecture** tienen un conjunto de valores que WMI controla, pero no se definen en los archivos de encabezado o biblioteca de tipos del SDK. Los valores se colocan en un parámetro de contexto para indicar a WMI que debe solicitar datos del proveedor no predeterminado.

A continuación se enumeran las marcas y sus valores posibles.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**
</dt> <dd>

Valor entero, 32 o 64, que especifica la versión de 32 o 64 bits.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**
</dt> <dd>

Valor booleano utilizado además de **\_ \_ ProviderArchitecture para** forzar la carga de la versión del proveedor especificada. Si la versión no está disponible, WMI devuelve el error 0x80041013, **wbemErrProviderLoadFailure** para Visual Basic **y WBEM \_ E PROVIDER \_ LOAD \_ \_ FAILURE** para C++. El valor predeterminado de esta marca cuando no se especifica es **FALSE.**

</dd> </dl>

En un sistema de 64 bits que tiene versiones en paralelo de un proveedor, una aplicación o script de 32 bits recibe automáticamente datos del proveedor de 32 bits, a menos que se proporcionan estas marcas e indican que se deben devolver los datos del proveedor de 64 bits.

## <a name="using-the-context-flags"></a>Uso de las marcas de contexto

Las aplicaciones de C++ pueden usar la interfaz [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) para comunicar el uso de un proveedor no predeterminado a WMI.

En scripting y Visual Basic, debe crear un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contenga las marcas para el parámetro *objWbemNamedValueSet* [**de SWbemServices.ExecMethod**](swbemservices-execmethod.md). Para obtener más información sobre cómo configurar los objetos de parámetros para esta llamada, vea Construir objetos [InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

Puede ejecutar scripts y aplicaciones de forma segura mediante las marcas de contexto en sistemas operativos anteriores, ya que WMI los omite en sistemas en los que no se implementan. Aunque existen versiones de 32 y 64 bits del proveedor del Registro del sistema, tenga en cuenta que solo existe una versión del repositorio WMI.

## <a name="accessing-the-default-registry-hive"></a>Acceso al subárbol del Registro predeterminado

En la siguiente serie de ejemplos se usa el proveedor del Registro [,](/previous-versions/windows/desktop/regprov/system-registry-provider)que tiene versiones en paralelo de 32 y 64 bits preinstaladas en sistemas operativos de 64 bits. En estos ejemplos, los clientes de 32 bits obtienen datos devueltos por el proveedor del nodo de 32 bits **HKEY \_ LOCAL MACHINE SOFTWARE \_ \\ \\ Wow6432Node \\ de Microsoft**. Los clientes de 64 bits obtienen datos devueltos por el proveedor del nodo de 64 bits **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ Logging**.

Los scripts muestran cómo llamar a los métodos de la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) del Registro a través [**de SWbemServices.ExecMethod**](swbemservices-execmethod.md) para obtener datos del subárbol del Registro de 32 bits.

El siguiente script obtiene datos del proveedor que coincide con el ancho de bits del autor de la llamada, en este caso 64 bits, porque es un script que se ejecuta en el host de script de Windows de 64 bits (WSH). El script obtiene el valor del nodo del Registro de 64 bits **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ WBEM \\ CIMOM \\ Logging** en lugar del nodo de 32 bits **HKEY LOCAL MACHINE SOFTWARE \_ \_ \\ \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



Si el **valor de** Registro del subárbol predeterminado se establece en 1, la salida del script debe tener un aspecto parecido al siguiente:

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Ejemplo: Solicitud específica del Subárbol del Registro de 32 bits en un equipo de 64 bits

En el siguiente ejemplo modificado del script predeterminado se usa la marca de cadena **\_ \_ ProviderArchitecture** para solicitar acceso a los datos del Registro de 32 bits en un equipo de 64 bits. El autor de la llamada está conectado al subárbol de 32 bits independientemente de si se trata de una aplicación de 32 o 64 bits.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Ejemplo: Forzar a WMI a acceder al Subárbol del Registro de 32 bits en un equipo de 64 bits

La siguiente modificación del script anterior mediante la adición de las marcas **\_ \_ ProviderArchitecture** y **\_ \_ RequiredArchitecture** al parámetro context obliga a WMI a cargar el proveedor de 32 bits y obtener datos de 32 bits. Si el proveedor no existe, se produce un error de carga del proveedor. El objeto de contexto se debe proporcionar en la conexión a WMI mediante una llamada a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
