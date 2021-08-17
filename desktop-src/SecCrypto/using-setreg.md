---
description: La herramienta SetReg establece el valor de las claves del Registro que controlan el comportamiento del proceso de comprobación del certificado Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Uso de SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0de37d236b978217d8c2a713e9595fbaad70afb69beb32cd0f5200738d2d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896742"
---
# <a name="using-setreg"></a>Uso de SetReg

La herramienta SetReg establece el valor de las claves del Registro que controlan el comportamiento del proceso de comprobación del certificado Authenticode. Estas claves, denominadas claves de estado de publicación de software, controlan si confiar en una raíz de prueba, permiten la aprobación sin conexión de certificados, prueban las fechas de expiración del certificado y realizan comprobaciones de revocación.

El comando siguiente muestra la sintaxis y las opciones para usar SetReg.

**setreg -?**

El siguiente comando hace que una raíz de prueba sea de confianza. De forma predeterminada, una raíz de prueba no es de confianza. Una vez realizados los cambios en los valores de clave, se muestra una lista del valor actual de todos los valores de clave. Si se **usa la opción -q,** no se muestran los valores de clave.

**setreg 1 TRUE**

El siguiente comando hace que una raíz de prueba no sea de confianza y hace que todas las comprobaciones comprueben la revocación. Se **usa la opción -q** para que no se muestre la lista de valores de clave.

**setreg -q 1 FALSE 3 TRUE**

> [!Note]  
> Los comandos, las opciones y los argumentos no distinguen mayúsculas de minúsculas.

 

 

 



