---
description: Para aplicar la transformación de personalización durante una instalación del producto, debe agregar una secuencia de información de resumen al archivo de transformación MNPtrans.mst generado en Generar una transformación de personalización.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Agregar información de resumen a la transformación de personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159194"
---
# <a name="adding-summary-information-to-customization-transform"></a>Agregar información de resumen a la transformación de personalización

Para aplicar la transformación de personalización durante una [](summary-information-stream.md) instalación del producto, debe agregar una secuencia de información de resumen al archivo de transformación MNPtrans.mst generado en Generar una transformación [de personalización.](generating-a-customization-transform.md)

Puede generar información de resumen para una transformación [**mediante MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) o [**el método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md). El siguiente fragmento de Sum.vbs muestra el método [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) y se usa con Windows host de script. Tenga en cuenta que en este ejemplo no se realiza ninguna validación y no se suprime ninguna condición de error.


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



Para crear y agregar información de resumen al archivo de transformación MNPtrans.mst que creó en Generación de una transformación de personalización, cambie los directorios [a](generating-a-customization-transform.md)la carpeta que contiene Gen.vbs, la base de datos original, la base de datos actualizada y la transformación, y escriba la línea de comandos siguiente.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**

Haga clic en MNP2000.msi icono para iniciar una instalación o use la siguiente línea de comandos.

**msiexec /i MNP2000.msi**

Esto instala el producto sin las personalizaciones. Para instalar con la personalización, escriba la siguiente línea de comandos. Tenga en cuenta que el valor de la [**propiedad TRANSFORMS**](transforms.md) hace referencia al archivo de transformación ubicado en el origen.

**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**

La característica Puerta no aparece en el árbol de selección de características y los componentes de la característica Puerta no se instalan incluso si se selecciona un tipo completo de instalación en la interfaz de usuario.

[Continuar](embedding-customization-transforms-as-substorage.md)

 

 



