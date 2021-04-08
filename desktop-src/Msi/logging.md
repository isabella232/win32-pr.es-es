---
description: Esta Directiva del sistema por equipo se usa solo si el registro no se ha habilitado mediante el &\# 0034;/l&\# 0034; opción de línea de comandos o por MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813843"
---
# <a name="logging-windows-installer"></a>Registro (Windows Installer)

Esta [Directiva del sistema](system-policy.md) por equipo se usa solo si la opción de línea de comandos "/l" o [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)no ha habilitado el registro. Si se establece la Directiva en este caso, el instalador crea un archivo de registro en% Temp% con el nombre aleatorio: MSI \* . Inicia. Especifique el modo de registro estableciendo el valor de la Directiva en una cadena de caracteres. Utilice los mismos caracteres para especificar la Directiva de modo de registro que usa la [opción de línea de comandos](command-line-options.md)"/l". Tenga en cuenta que no puede usar "+" y " \* " para la Directiva.

El modo de registro se puede establecer mediante la Directiva, una opción de línea de comandos o mediante programación. Para obtener más información acerca de todos los métodos que están disponibles para establecer el modo de registro, consulte el [registro normal](normal-logging.md) en la sección [registro de Windows Installer](windows-installer-logging.md) .

Puede evitar que se escriba información confidencial, como contraseñas, en el archivo de registro y se haga visible. Para obtener más información, consulte [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md) .

## <a name="registry-key"></a>Clave del Registro

Establezca el valor denominado Logging en la siguiente clave del registro.

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**Registro \_ SZ**

 

 



