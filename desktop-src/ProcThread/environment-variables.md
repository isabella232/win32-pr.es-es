---
description: 'Cada proceso tiene un bloque de entorno que contiene un conjunto de variables de entorno y sus valores. Hay dos tipos de variables de entorno: variables de entorno de usuario (establecidas para cada usuario) y variables de entorno del sistema (establecidas para todos).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Variables de entorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f50226d12286d01c77025d1cc38e33e2778392a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073884"
---
# <a name="environment-variables"></a>Variables de entorno

Cada proceso tiene un bloque de entorno que contiene un conjunto de variables de entorno y sus valores. Hay dos tipos de variables de entorno: variables de entorno de usuario (establecidas para cada usuario) y variables de entorno del sistema (establecidas para todos).

De forma predeterminada, un proceso secundario hereda las variables de entorno de su proceso primario. Los programas iniciados por el procesador de comandos heredan las variables de entorno del procesador de comandos. Para especificar un entorno diferente para un proceso secundario, cree un nuevo bloque de entorno y pásle un puntero como parámetro a la [**función CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)

El procesador de comandos proporciona el **comando set** para mostrar su bloque de entorno o para crear nuevas variables de entorno. También puede ver o modificar las  variables de entorno seleccionando Sistema en el Panel de control **,** seleccionando Configuración avanzada del sistema y haciendo clic en Variables **de entorno**.

Cada bloque de entorno contiene las variables de entorno en el formato siguiente:<dl> *Var1* = *Valor1* \\ 0  
*Var2* = *Valor2* \\ 0  
*Var3* = *Valor3* \\ 0  
...  
*VarN* = *ValueN* \\ 0 \\ 0  
</dl>

El nombre de una variable de entorno no puede incluir un signo igual (=).

La [**función GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) devuelve un puntero al bloque de entorno del proceso de llamada. Esto debe tratarse como un bloque de solo lectura; no lo modifique directamente. En su lugar, use [**la función SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) para cambiar una variable de entorno. Cuando haya terminado con el bloque de entorno obtenido de **GetEnvironmentStrings,** llame a la [**función FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) para liberar el bloque.

Llamar [**a SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) no tiene ningún efecto en las variables de entorno del sistema. Para agregar o modificar variables de entorno del sistema mediante programación, agrégolas a la clave del Registro **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ Environment** y, a continuación, difunda un mensaje [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) con *lParam* establecido en la cadena "Environment". Esto permite a las aplicaciones, como el shell, recoger las actualizaciones.

El tamaño máximo de una variable de entorno definida por el usuario es de 32 767 caracteres. No hay ninguna limitación técnica en el tamaño del bloque de entorno. Sin embargo, hay límites prácticos en función del mecanismo utilizado para acceder al bloque. Por ejemplo, un archivo por lotes no puede establecer una variable que sea mayor que la longitud máxima de la línea de comandos.

**Windows Server 2003 y Windows XP:** El tamaño máximo del bloque de entorno para el proceso es de 32 767 caracteres. A partir Windows Vista y Windows Server 2008, no hay ninguna limitación técnica en el tamaño del bloque de entorno.

La [**función GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) determina si se define una variable especificada en el entorno del proceso de llamada y, si es así, cuál es su valor.

Para recuperar una copia del bloque de entorno para un usuario determinado, use la [**función CreateEnvironmentBlock.**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock)

Para expandir las cadenas de variables de entorno, use la [**función ExpandEnvironmentStrings.**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cambio de variables de entorno](changing-environment-variables.md)
</dt> <dt>

[Variables de entorno de usuario](../shell/user-environment-variables.md)
</dt> </dl>

 

 
