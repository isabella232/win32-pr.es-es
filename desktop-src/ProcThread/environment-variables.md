---
description: 'Cada proceso tiene un bloque de entorno que contiene un conjunto de variables de entorno y sus valores. Hay dos tipos de variables de entorno: las variables de entorno de usuario (establecidas para cada usuario) y las variables de entorno del sistema (establecidas para todos).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Variables de entorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f50226d12286d01c77025d1cc38e33e2778392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677862"
---
# <a name="environment-variables"></a>Variables de entorno

Cada proceso tiene un bloque de entorno que contiene un conjunto de variables de entorno y sus valores. Hay dos tipos de variables de entorno: las variables de entorno de usuario (establecidas para cada usuario) y las variables de entorno del sistema (establecidas para todos).

De forma predeterminada, un proceso secundario hereda las variables de entorno de su proceso primario. Los programas iniciados por el procesador de comandos heredan las variables de entorno del procesador de comandos. Para especificar un entorno diferente para un proceso secundario, cree un nuevo bloque de entorno y pase un puntero a él como parámetro a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

El procesador de comandos proporciona el comando **set** para mostrar su bloque de entorno o para crear nuevas variables de entorno. También puede ver o modificar las variables de entorno; para ello, seleccione **sistema** en el **Panel de control**, seleccione **Configuración avanzada del sistema** y, a continuación, haga clic en **variables de entorno**.

Cada bloque de entorno contiene las variables de entorno con el siguiente formato:<dl> *Var1* = *Valor1* \\ 0,1  
*Var2* = *Valor2* \\ 0,1  
*Var3* = *Value3* \\ 0,1  
...  
*VarN* = *Valor de* \\ 0 \\ 0  
</dl>

El nombre de una variable de entorno no puede incluir un signo igual (=).

La función [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) devuelve un puntero al bloque de entorno del proceso de llamada. Esto se debe tratar como un bloque de solo lectura; no lo modifique directamente. En su lugar, use la función [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) para cambiar una variable de entorno. Cuando haya terminado con el bloque de entorno Obtenido de **GetEnvironmentStrings**, llame a la función [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) para liberar el bloque.

La llamada a [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) no tiene ningún efecto en las variables de entorno del sistema. Para agregar o modificar mediante programación variables de entorno del sistema, agréguelas a la clave del registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager \\** y, a continuación, difunde un mensaje de [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) con *lParam* establecido en la cadena "Environment". Esto permite a las aplicaciones, como el Shell, seleccionar las actualizaciones.

El tamaño máximo de una variable de entorno definida por el usuario es de 32.767 caracteres. No hay ninguna limitación técnica en cuanto al tamaño del bloque de entorno. Sin embargo, hay límites prácticos según el mecanismo utilizado para tener acceso al bloque. Por ejemplo, un archivo por lotes no puede establecer una variable que sea mayor que la longitud máxima de la línea de comandos.

**Windows Server 2003 y Windows XP:** El tamaño máximo del bloque de entorno para el proceso es de 32.767 caracteres. A partir de Windows Vista y Windows Server 2008, no hay ninguna limitación técnica en cuanto al tamaño del bloque de entorno.

La función [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) determina si una variable especificada está definida en el entorno del proceso de llamada y, en ese caso, cuál es su valor.

Para recuperar una copia del bloque de entorno para un usuario determinado, use la función [**CreateEnvironmentBlock**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) .

Para expandir cadenas de variables de entorno, utilice la función [**ExpandEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cambiar variables de entorno](changing-environment-variables.md)
</dt> <dt>

[Variables de entorno de usuario](../shell/user-environment-variables.md)
</dt> </dl>

 

 
