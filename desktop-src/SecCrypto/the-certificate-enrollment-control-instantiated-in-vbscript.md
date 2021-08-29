---
description: Ejemplo Visual Basic Scripting Edition (VBScript) que usa la etiqueta OBJECT para crear una instancia del objeto Control de inscripción de certificados.
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: Control de inscripción de certificados con instancias de VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 68de4532e00f95156b0016a55d4ae7b6374936e82ef26ee04cfbf4dc0e4c72c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897316"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a>Control de inscripción de certificados con instancias de VBScript

En el Visual Basic ejemplo de Scripting Edition (VBScript) se usa la etiqueta OBJECT para crear una instancia del objeto Control de inscripción de certificados. El objeto se libera de la memoria cuando sale del ámbito.


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<BR>
Certificate Enrollment Control Instantiation Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare a local variable.
Dim varName
' Enable error handling.
On Error Resume Next
' Attempt to use the control, in this case to retrieve a property.
varName = Enroll.MyStoreName
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error!")
    Err.clear
else
    ' The control property was successfully retrieved,
    ' display the property value.
    varName = "MyStoreName is " & varName
    MsgBox( varName )
end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 



