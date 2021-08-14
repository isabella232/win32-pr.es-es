---
description: Esta directiva de sistema por máquina solo se usa si el registro no se ha habilitado mediante la opción de línea de comandos &\# 0034;/L&\# 0034; o msiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49993419b03e3c092fdf4d2b6d9d118ca4dc2d3d641c82c4fc829cbfd6b68c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945640"
---
# <a name="logging-windows-installer"></a>Registro (Windows instalador)

Esta directiva [de](system-policy.md) sistema por máquina solo se usa si el registro no se ha habilitado mediante la opción de línea de comandos "/L" o [**msiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Si la directiva se establece en este caso, el instalador crea un archivo de registro en %temp% con el nombre aleatorio: MSI \* . Registro. Especifique el modo de registro estableciendo el valor de directiva en una cadena de caracteres. Use los mismos caracteres para especificar la directiva de modo de registro que usa la opción de línea de comandos ["/L".](command-line-options.md) Tenga en cuenta que no puede usar "+" y \* "" para la directiva.

El modo de registro se puede establecer mediante directiva, una opción de línea de comandos o mediante programación. Para obtener más información sobre todos los métodos disponibles para establecer el modo de registro, vea [Registro normal](normal-logging.md) en la [Windows registro](windows-installer-logging.md) del instalador.

Puede evitar que la información confidencial, por ejemplo, las contraseñas, se introduce en el archivo de registro y se hace visible. Para obtener más información, vea [Impedir que la información confidencial se escriba en el archivo de registro.](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Clave del Registro

Establezca el valor denominado Registro en la siguiente clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ SZ**

 

 



