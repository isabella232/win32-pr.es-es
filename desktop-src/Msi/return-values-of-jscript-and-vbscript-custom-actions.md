---
description: Las acciones personalizadas escritas en JScript o Visual Basic, Scripting Edition (VBScript) pueden llamar a una función opcional. Estas funciones deben devolver uno de los valores que se muestran en la tabla siguiente.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valores devueltos de las acciones personalizadas de JScript y VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666800"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Valores devueltos de las acciones personalizadas de JScript y VBScript

Las acciones personalizadas escritas en JScript o Visual Basic, Scripting Edition (VBScript) pueden llamar a una función opcional. Estas funciones deben devolver uno de los valores que se muestran en la tabla siguiente.



| Valor devuelto              | Value        | Descripción                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Acción no ejecutada.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | Acción completada correctamente.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Finalización prematura por usuario.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Error irrecuperable. Se devuelve si se produce un error durante el análisis o la ejecución de JScript o VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Secuencia suspendida que se reanudará más adelante.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Omitir las acciones restantes. No es un error.                                                                      |



 

Tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 (uno) en el archivo de registro, significa que la acción devolvió msiDoActionStatusSuccess. Para obtener más información sobre esta traducción, consulte [registro de valores devueltos de acciones](logging-of-action-return-values.md).

Para devolver un valor distinto de Success desde una acción personalizada de script, debe usar un destino de función para la acción personalizada. La función de destino se especifica en la columna de destino de la [tabla CustomAction](customaction-table.md).

En el ejemplo de script siguiente se muestra cómo devolver Success o Failure desde una acción personalizada de VBScript.


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



Si este VBScript se incrustó en la [tabla binaria](binary-table.md) del paquete de instalación como MyCA.vbs, la entrada de la [tabla CustomAction](customaction-table.md) del script sería la siguiente:



| Acción         | Tipo | Source   | Destino       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



