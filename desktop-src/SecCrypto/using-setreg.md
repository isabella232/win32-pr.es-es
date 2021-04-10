---
description: La herramienta SetReg establece el valor de las claves del registro que controlan el comportamiento del proceso de comprobación de certificados Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Usar SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155084"
---
# <a name="using-setreg"></a>Usar SetReg

La herramienta SetReg establece el valor de las claves del registro que controlan el comportamiento del proceso de comprobación de certificados Authenticode. Estas claves, denominadas claves de estado de publicación de software, controlan si se confía en una raíz de prueba, permiten la aprobación sin conexión de certificados, las fechas de expiración de certificado de prueba y realizan comprobaciones de revocación.

El siguiente comando muestra la sintaxis y las opciones para usar SetReg.

**setreg-?**

El comando siguiente hace que se confíe en una raíz de prueba. De forma predeterminada, una raíz de prueba no es de confianza. Una vez realizados los cambios en los valores de clave, se muestra una lista del valor actual de todos los valores de clave. Si se usa la opción **-q** , no se muestran los valores de clave.

**setreg 1 TRUE**

El comando siguiente hace que una raíz de prueba no sea de confianza y hace que toda la comprobación Compruebe la revocación. Se usa la opción **-q** para que no se muestre la lista de valores de clave.

**setreg-q 1 falso 3 TRUE**

> [!Note]  
> Los comandos, las opciones y los argumentos no distinguen mayúsculas de minúsculas.

 

 

 



