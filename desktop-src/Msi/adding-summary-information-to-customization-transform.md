---
description: Para aplicar la transformación de personalización durante una instalación del producto, debe agregar una secuencia de información de resumen al archivo de transformación MNPtrans. MST generado en la generación de una transformación de personalización.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Agregar información de resumen a la transformación de personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652625"
---
# <a name="adding-summary-information-to-customization-transform"></a>Agregar información de resumen a la transformación de personalización

Para aplicar la transformación de personalización durante una instalación del producto, debe agregar una [secuencia de información de Resumen](summary-information-stream.md) al archivo de transformación MNPtrans. MST generado en la generación de [una transformación de personalización](generating-a-customization-transform.md).

Puede generar información de resumen para una transformación mediante [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) o el [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md). El siguiente fragmento de código, Sum.vbs, ilustra el [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) y es para su uso con Windows Script Host. Tenga en cuenta que en este ejemplo no se realiza ninguna validación y no se suprime ninguna condición de error.


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



Para crear y agregar información de resumen al archivo de transformación MNPtrans. MST que creó en [generación de una transformación de personalización](generating-a-customization-transform.md), cambie los directorios a la carpeta que contiene Gen.vbs, la base de datos original, la base de datos actualizada y la transformación, y escriba la siguiente línea de comandos.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

Haga clic en el icono de MNP2000.msi para iniciar una instalación o use la siguiente línea de comandos.

**msiexec/i MNP2000.msi**

Esto instala el producto sin las personalizaciones. Para instalar con la personalización, escriba la siguiente línea de comandos. Tenga en cuenta que el valor de la propiedad [**TRANSformations**](transforms.md) hace referencia al archivo de transformación ubicado en el origen.

**msiexec/i MNP2000.msi transformaciones = MNPtrans. MST**

La característica de puerta no aparece en el árbol de selección de características y los componentes de la característica de puerta no se instalan incluso si se selecciona un tipo de instalación completo en la interfaz de usuario.

[Continuar](embedding-customization-transforms-as-substorage.md)

 

 



