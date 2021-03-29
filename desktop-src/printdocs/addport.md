---
description: La función AddPort agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de Puerto exporta la función AddPort.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Función AddPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912962"
---
# <a name="addport-function"></a>AddPort función)

La función **AddPort** agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de Puerto exporta la función **AddPort** .

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del servidor al que está conectado el puerto. Si este parámetro es **null**, el puerto es local.

</dd> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo **AddPort** .

</dd> <dt>

*pMonitorName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el monitor asociado al puerto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

La función **AddPort** examina la red para buscar los puertos existentes y muestra un cuadro de diálogo para el usuario. La función **AddPort** debe validar el nombre de puerto especificado por el usuario mediante una llamada a [**EnumPorts**](enumports.md) para asegurarse de que no existe ningún nombre duplicado.

El autor de la llamada de la función **AddPort** debe tener acceso al servidor \_ \_ para administrar el acceso al servidor al que está conectado el puerto.

Para agregar un puerto sin mostrar un cuadro de diálogo, llame a la función **XcvData** en lugar de a **AddPort**. Para obtener más información acerca de **XcvData**, vea el kit de desarrollo de controladores (DDK) de Microsoft Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **AddPortW** (Unicode) y **AddPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




