---
description: La función SetForm establece la información del formulario para la impresora especificada.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Función SetForm (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568601"
---
# <a name="setform-function"></a>Función SetForm

La **función SetForm** establece la información del formulario para la impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que se establece la información del formulario. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pFormName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del formulario para el que se establece la información del formulario.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que *apunta pForm.* Este valor debe ser 1 o 2.

</dd> <dt>

*pForm* \[ En\]
</dt> <dd>

Puntero a una [**estructura FORM \_ INFO \_ 1**](form-info-1.md) [**o FORM INFO \_ \_ 2.**](form-info-2.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

**Se puede llamar** a SetForm varias veces para una instancia de [**FORM INFO \_ \_ 2**](form-info-2.md)existente, cada llamada agrega pares adicionales de **valores pDisplayName** y **wLangId.** Todas las versiones de idioma del formulario obtienen los valores **Size** e **ImageableArea** de **FORM INFO \_ \_ 2** en la llamada más reciente a **SetForm**.

Si el autor de la llamada es remoto y *el* nivel es 2, el valor **StringType** de [**FORM INFO \_ \_ 2**](form-info-2.md) no puede ser STRING \_ MUIDLL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetFormW** (Unicode) y **SetFormA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**FORM \_ INFO \_ 1**](form-info-1.md)
</dt> <dt>

[**FORM \_ INFO \_ 2**](form-info-2.md)
</dt> </dl>

 

 




