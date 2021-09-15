---
description: Describe cómo usar la Herramienta de búsqueda de errores de Microsoft para buscar explicaciones de texto de códigos de error hexadecimales en Windows.
title: Herramienta de búsqueda de errores de Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568569"
---
# <a name="the-microsoft-error-lookup-tool"></a>Herramienta de búsqueda de errores de Microsoft

La Herramienta de búsqueda de errores de Microsoft muestra el texto del mensaje asociado a un código de estado hexadecimal (u otro código). Este texto se define en varios archivos de encabezado de código fuente de Microsoft, como Winerror.h, Setupapi.h, y así sucesivamente.

Microsoft firma digitalmente la herramienta. A continuación se muestra la información sha256 para la descarga de archivos:  

|Algoritmo |Hash |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Los entornos empresariales pueden restringir qué archivos se pueden ejecutar y desde dónde. Antes de descargar y ejecutar esta herramienta, compruebe los detalles siguientes:
> - ¿Tiene que tener permiso o una excepción de seguridad para descargar o ejecutar la herramienta?
> - ¿Puede almacenar y ejecutar esta herramienta en el equipo (por ejemplo, en la carpeta Documentos)? ¿O tiene que almacenar y ejecutar la herramienta en un equipo especializado, como un servidor de archivos central?

## <a name="usage"></a>Uso

1. Para descargar la herramienta, seleccione [este vínculo.](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)
1. Si no especificó una ubicación en el paso 1, vaya a la carpeta de descarga y copie o mueva el archivo descargado (Err_6.4.5.exe) a la carpeta en la que almacenará la herramienta. No es necesario expandir ni instalar el archivo.
   > [!NOTE]
   > Si copia o mueve el archivo a una carpeta que aparece en la variable de entorno **Path** del sistema operativo, funcionará en cualquier símbolo del sistema.

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

Tenga en cuenta que se trata de una herramienta "a un momento dado". La Herramienta de búsqueda de errores de Microsoft descodifica la mayoría de los códigos de error de Microsoft a partir de la fecha en que se compiló la herramienta. A medida que las nuevas versiones Windows agregar nuevos códigos de error y eventos, es posible que tenga que descargar una nueva versión de la herramienta de búsqueda de errores. Compruebe en el Centro de descarga de Microsoft una nueva versión o vea [Códigos de error](system-error-codes.md).
