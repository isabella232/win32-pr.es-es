---
description: El método LastErrorRecord del objeto Installer devuelve un objeto Record que contiene parámetros de error para el error más reciente de la función que produjo el registro de errores.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Método Installer.LastErrorRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142114"
---
# <a name="installerlasterrorrecord-method"></a>Método Installer.LastErrorRecord

El **método LastErrorRecord** del objeto [**Installer**](installer-object.md) devuelve un objeto [**Record**](record-object.md) que contiene parámetros de error para el error más reciente de la función que produjo el registro de errores.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El [**objeto Record**](record-object.md) se restablece después de la ejecución de esta función de cualquier función que genere un registro de error.

Solo las siguientes funciones designadas generan un registro de error:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Confirmar**](database-commit.md)
-   [**Openview**](database-openview.md)
-   [**Importar**](database-import.md)
-   [**Exportación**](database-export.md)
-   [**Combinar**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Ejecutar**](view-execute.md)
-   [**Modificar**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

En el ejemplo siguiente de VBScript se usa una llamada a [**OpenDatabase**](installer-opendatabase.md) para mostrar cómo obtener información de error extendida de uno de los métodos o propiedades que admiten **el método LastErrorRecord.** El ejemplo crea un mensaje de error cuando se produce un error **en el método OpenDatabase.** El **objeto Err** se usa para determinar si se encontró un error.


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




