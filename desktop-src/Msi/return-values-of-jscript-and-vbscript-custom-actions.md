---
description: Las acciones personalizadas escritas JScript o Visual Basic, Scripting Edition (VBScript) puede llamar a una función opcional. Estas funciones deben devolver uno de los valores que se muestran en la tabla siguiente.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valores devueltos de JScript y acciones personalizadas de VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50a2b225c59b0e4d1787f2eaceeb094d6fb2abe7f9d9600822b6295ef2dd273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626095"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Valores devueltos de JScript y acciones personalizadas de VBScript

Las acciones personalizadas escritas JScript o Visual Basic, Scripting Edition (VBScript) puede llamar a una función opcional. Estas funciones deben devolver uno de los valores que se muestran en la tabla siguiente.



| Valor devuelto              | Value        | Descripción                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Acción no ejecutada.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | La acción se completó correctamente.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Terminación prematura por parte del usuario.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Error irrecuperable. Se devuelve si se produce un error durante el análisis o la ejecución del JScript o VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Secuencia suspendida que se reanudará más adelante.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Omita las acciones restantes. No es un error.                                                                      |



 

Tenga en cuenta Windows instalador traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro. Por ejemplo, si el valor devuelto de la acción aparece como 1 (uno) en el archivo de registro, significa que la acción devolvió msiDoActionStatusSuccess. Para obtener más información sobre esta traducción, vea [Registro de valores devueltos de acción](logging-of-action-return-values.md).

Para devolver un valor distinto de correcto de una acción personalizada de script, debe usar un destino de función para la acción personalizada. La función de destino se especifica en la columna Target de [la tabla CustomAction](customaction-table.md).

En el ejemplo de script siguiente se muestra cómo devolver una acción personalizada de VBScript correcta o con errores.


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



Si este VBScript se incrustase en la tabla [Binary](binary-table.md) del paquete de instalación como MyCA.vbs, la [entrada CustomAction Table](customaction-table.md) del script sería la siguiente:



| Acción         | Tipo | Source   | Destino       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



