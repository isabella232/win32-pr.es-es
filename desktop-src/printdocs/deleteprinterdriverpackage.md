---
description: Elimina un paquete de controladores de impresora del almacén de controladores.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Función DeletePrinterDriverPackage (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: d7247f4f0ef4d1f77f00664792d0b7b36bc991b19d437017b54db676731ccc70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112555"
---
# <a name="deleteprinterdriverpackage-function"></a>Función DeletePrinterDriverPackage

Elimina un paquete de controladores de impresora del almacén de controladores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszServer* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica el nombre del servidor de impresión del que se elimina el paquete de controladores. Un **valor de** puntero NULL significa el equipo local.

</dd> <dt>

*pszInfPath* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica la ruta de acceso al \* archivo .inf del controlador.

</dd> <dt>

*pszEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

S \_ Ok, si la operación se realiza correctamente.

E \_ ACCESSDENIED, si el paquete se envió con Windows.

HRESULT \_ CODE(ERROR \_ PRINT DRIVER PACKAGE IN \_ \_ \_ \_ USE), si se usa el paquete.

De lo **contrario, HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El almacén de controladores suele ser %windir% \\ inf o %windir% \\ System32 \\ DriverStore \\ FileRepository.

Un paquete de controladores que se incluye Windows no se puede quitar con esta función.

El usuario debe tener privilegios de administración de impresoras.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterDriverPackageW** (Unicode) y **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

