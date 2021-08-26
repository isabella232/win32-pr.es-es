---
description: La función AddPort agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de puerto exporta la función AddPort.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Función AddPort (Winspool.h)
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
ms.openlocfilehash: abbb2e4b836c64ddff47c92681e32bd0d5f9f0c38224d6c710fb10bc3435ac96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112695"
---
# <a name="addport-function"></a>Función AddPort

La **función AddPort** agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de puerto exporta la función **AddPort.**

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

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del servidor al que está conectado el puerto. Si este parámetro es **NULL,** el puerto es local.

</dd> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador de la ventana primaria del **cuadro de diálogo AgregarPort.**

</dd> <dt>

*pMonitorName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el monitor asociado al puerto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La **función AddPort** examina la red para buscar puertos existentes y muestra un cuadro de diálogo para el usuario. La **función AddPort** debe validar el nombre de puerto especificado por el usuario llamando a [**EnumPorts**](enumports.md) para asegurarse de que no existe ningún nombre duplicado.

El autor de la llamada **de la función AddPort** debe tener acceso SERVER ACCESS ADMINISTER al servidor al \_ que está conectado el \_ puerto.

Para agregar un puerto sin mostrar un cuadro de diálogo, llame a la **función XcvData** en lugar de **AddPort**. Para obtener más información sobre **XcvData,** vea Microsoft Windows Driver Development Kit (DDK).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
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

 

 




