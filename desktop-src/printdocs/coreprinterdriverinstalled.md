---
description: La función CorePrinterDriverInstalled notifica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Función CorePrinterDriverInstalled (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083024"
---
# <a name="coreprinterdriverinstalled-function"></a>CorePrinterDriverInstalled función)

La función **CorePrinterDriverInstalled** notifica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszServer* \[ de\]
</dt> <dd>

Puntero a una cadena constante y terminada en null que especifica el nombre del servidor de impresión. Use **null** para el equipo local.

</dd> <dt>

*pszEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena constante, terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **null**.

</dd> <dt>

*CoreDriverGUID* \[ de\]
</dt> <dd>

GUID del controlador de impresora principal.

</dd> <dt>

*ftDriverDate* \[ de\]
</dt> <dd>

La fecha del controlador de impresora principal.

</dd> <dt>

*dwlDriverVersion* \[ de\]
</dt> <dd>

Versión del controlador de impresora principal.

</dd> <dt>

*pbDriverInstalled* \[ enuncia\]
</dt> <dd>

Un puntero a **true** si se instala el controlador, o una versión más reciente, **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **CorePrinterDriverInstalledW** (Unicode) y **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

