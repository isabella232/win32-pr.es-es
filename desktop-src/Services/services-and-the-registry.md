---
description: Un servicio no debe tener acceso a HKEY \_ CURRENT USER o HKEY CLASSES ROOT, especialmente al \_ \_ \_ suplantar a un usuario. En su lugar, use las funciones RegOpenCurrentUser o RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Servicios y el Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170818"
---
# <a name="services-and-the-registry"></a>Servicios y el Registro

Un servicio no debe tener acceso **a HKEY \_ CURRENT USER \_ o** **HKEY CLASSES \_ \_ ROOT,** especialmente al suplantar a un usuario. En su lugar, use [**las funciones RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) [**o RegOpenUserClassesRoot.**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot)

Si intenta acceder a **HKEY \_ CURRENT \_ USER** o **HKEY \_ CLASSES \_ ROOT** desde un servicio, puede producir un error, o puede parecer que funciona, pero hay una pérdida subyacente que puede provocar problemas al cargar o descargar el perfil de usuario.

 

 
