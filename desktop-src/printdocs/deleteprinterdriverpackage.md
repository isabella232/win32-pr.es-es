---
description: Elimina un paquete de controladores de impresora del almacén de controladores.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Función DeletePrinterDriverPackage (winspool. h)
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
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706295"
---
# <a name="deleteprinterdriverpackage-function"></a>DeletePrinterDriverPackage función)

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

*pszServer* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión del que se va a eliminar el paquete de controladores. Un valor de puntero **nulo** significa el equipo local.

</dd> <dt>

*pszInfPath* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la ruta de acceso al \* archivo. inf del controlador.

</dd> <dt>

*pszEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

S \_ correcto, si la operación se realiza correctamente.

E \_ ACCESSDENIED, si el paquete se incluyó con Windows.

\_Código HRESULT (error \_ \_ \_ \_ de paquete de controlador de impresión en \_ uso), si se está usando el paquete.

De lo contrario, el **valor HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El almacén de controladores suele ser% WINDIR% \\ inf o% WINDIR% \\ system32 \\ DriverStore \\ FileRepository.

No se puede quitar un paquete de controladores incluido con Windows con esta función.

El usuario debe tener privilegios de administración de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterDriverPackageW** (Unicode) y **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

