---
description: Describe cómo usar la herramienta de búsqueda de errores de Microsoft para buscar explicaciones de texto de códigos de error hexadecimales en Windows.
title: Herramienta de búsqueda de errores de Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720278"
---
# <a name="the-microsoft-error-lookup-tool"></a>Herramienta de búsqueda de errores de Microsoft

La herramienta de búsqueda de errores de Microsoft muestra el texto del mensaje que está asociado a un código de estado hexadecimal (u otro código). Este texto se define en varios archivos de encabezado de código fuente de Microsoft, como Winerror. h, setupapi. h, etc.

La herramienta está firmada digitalmente por Microsoft. A continuación se encuentra la información de SHA256 para la descarga de archivos:  

|Algoritmo |Hash |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Los entornos empresariales pueden restringir qué archivos pueden ejecutarse y desde dónde. Antes de descargar y ejecutar esta herramienta, compruebe los detalles siguientes:
> - ¿Tiene que tener permiso o una excepción de seguridad para descargar o ejecutar la herramienta?
> - ¿Puede almacenar y ejecutar esta herramienta en el equipo (por ejemplo, en la carpeta documentos)? ¿O tiene que almacenar y ejecutar la herramienta en un equipo especializado, como un servidor de archivos central?

## <a name="usage"></a>Uso

1. Descargue la herramienta seleccionando [este vínculo](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).
1. Si no especificó una ubicación en el paso 1, vaya a la carpeta de descarga y copie o mueva el archivo descargado (Err_6.4.5.exe) a la carpeta en la que se almacenará la herramienta. No es necesario expandir ni instalar el archivo.
   > [!NOTE]
   > Si copia o mueve el archivo a una carpeta que aparece en la variable de entorno **path** de su sistema operativo, funcionará en cualquier símbolo del sistema.

1. Abra una ventana de símbolo del sistema. Si es necesario, cambie el directorio a la ubicación de la herramienta de búsqueda de errores.
1. Ejecute el siguiente comando:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > En este comando, \<*error code*> representa el código hexadecimal que desea buscar.

## <a name="examples"></a>Ejemplos

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a>Más información

Tenga en cuenta que se trata de una herramienta "momento dado". La herramienta de búsqueda de errores de Microsoft descodifica la mayoría de los códigos de error de Microsoft a partir de la fecha en la que se compiló la herramienta. A medida que nuevas versiones de Windows agregan nuevos eventos y códigos de error, es posible que tenga que descargar una nueva versión de la herramienta de búsqueda de errores. Consulte el centro de descarga de Microsoft para obtener una nueva versión o vea los [códigos de error](system-error-codes.md).
