---
description: Un ejemplo de Visual Basic Scripting Edition (VBScript) que usa la etiqueta de objeto para crear una instancia del objeto de control de inscripción de certificados.
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: El control de inscripción de certificados del que se ha creado una instancia en VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da14c55a3c9005f820be8f8d60026bc31ac4920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001209"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a>El control de inscripción de certificados del que se ha creado una instancia en VBScript

En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se usa la etiqueta de objeto para crear una instancia del objeto de control de inscripción de certificados. El objeto se libera de la memoria cuando sale del ámbito.


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



 

 



