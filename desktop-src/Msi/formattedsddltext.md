---
description: Un campo de base de datos del tipo de datos FormattedSDDLText contiene una cadena de texto que describe un descriptor de seguridad mediante el lenguaje de definición de descriptores de seguridad (SDDL). El campo SDDLText de la tabla MsiLockPermissionsEx usa este tipo de datos para proteger un objeto seleccionado. Tenga en cuenta que el campo SDDLText de la tabla MsiLockPermissionsEx no es compatible con las propiedades públicas o privadas.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ddfeac55f05ebea5f1603def6adcbac32aa9d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666803"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Un campo de base de datos del tipo de datos **FormattedSDDLText** contiene una cadena de texto que describe un descriptor de seguridad mediante el [lenguaje de definición de descriptores de seguridad](../secauthz/security-descriptor-definition-language.md) (SDDL). El campo SDDLText de la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) usa este tipo de datos para proteger un objeto seleccionado. Tenga en cuenta que el campo SDDLText de la tabla MsiLockPermissionsEx no es compatible con las propiedades públicas o privadas.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este tipo de datos está disponible a partir de Windows Installer 5,0.

El tipo de datos **FormattedSDDLText** puede contener una cadena SDDL escrita en un [formato de cadena de descriptor de seguridad](../secauthz/security-descriptor-string-format.md)válido. Para obtener más información sobre SDDL, consulte la sección [Access Control](../secauthz/access-control.md) del [Kit de desarrollo de software (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/). Además, una cadena de texto **FormattedSDDLText** puede usar corchetes angulares (<>) para contener el dominio y el nombre de usuario del usuario cuyo SID de cuenta se va a determinar.

Si el usuario que tiene el nombre de usuario *SampleUser* pertenece a un dominio denominado *SampleDomain*, el valor **FormattedSDDLText** puede identificar al propietario mediante la cadena SID, el nombre de usuario y el nombre de dominio, o las variables de entorno de Windows. Por ejemplo, las siguientes cadenas serían posibles.

<dl> O:*\_ \_ cadena de SID de propietario* G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; *\_ \_ cadena de SID de propietario*) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD  
O: <*SampleDomain \\ SAMPLEUSER*>G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; <*SampleDomain \\ SampleUser*>) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD  
O: <\[ % USERDOMAIN \] \\ \[ % username \]>G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; <\[ % USERDOMAIN \] \\ \[ % username \]>) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD
</dl>

 

 
