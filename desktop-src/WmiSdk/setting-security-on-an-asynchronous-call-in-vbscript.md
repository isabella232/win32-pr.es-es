---
description: Normalmente, el rendimiento de las llamadas sincrónicas es adecuado para la mayoría de las situaciones.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Establecer la seguridad en una llamada asincrónica en VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717041"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Establecer la seguridad en una llamada asincrónica en VBScript

Normalmente, el rendimiento de las llamadas [*sincrónicas*](gloss-s.md) es adecuado para la mayoría de las situaciones. Por lo general, las llamadas asincrónicas no son una práctica recomendada para los scripts. Sin embargo, si se deben realizar llamadas asincrónicas, se puede establecer un valor del registro para forzar a WMI a realizar comprobaciones de acceso en llamadas asincrónicas.


El valor del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla si WMI comprueba un nivel de autenticación aceptable al devolver los datos de una llamada asincrónica. La devolución de llamada se puede devolver en un nivel de autenticación inferior al de la llamada asincrónica original. De forma predeterminada, este valor se establece en cero para que no se comprueban las devoluciones de llamada. Para proteger las llamadas asincrónicas en scripting, debe establecer la clave del registro en 1 (uno).

Los scripts pueden usar los métodos [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) y [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) del objeto de registro [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para cambiar la configuración del valor del registro **UnsecAppAccessControlDefault** . Para obtener más información acerca de los niveles de autenticación y suplantación necesarios para el acceso remoto, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>Para establecer la seguridad de llamada asincrónica en VBScript

En el ejemplo de código de VBScript siguiente se muestra cómo cambiar el valor del registro para controlar la autenticación WMI de las devoluciones de llamada.

El script cambia el valor de **UnsecAppAccessControlDefault** de cero a uno, o bien, si el valor ya está establecido, de uno a cero. Cero es el valor predeterminado en un sistema recién instalado. Una vez establecida la marca, la configuración se mantiene en el reinicio o el reinicio de WMI.

El script usa un objeto [**SWbemMethod. Parameters**](swbemmethod-inparameters.md) y [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) para llamar a [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) y [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov). Para obtener más información sobre cómo establecer los valores **de un objeto Parameters** , vea [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Para obtener un ejemplo de una llamada al registro mediante [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), vea [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
