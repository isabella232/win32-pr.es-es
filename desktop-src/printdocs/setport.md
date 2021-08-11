---
description: La función SetPort establece el estado asociado a un puerto de impresora.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Función SetPort (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e3414d0566203aa51d78c6b7d4b0463cee5765bae8c35c083a959088b6559df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234035"
---
# <a name="setport-function"></a>Función SetPort

La **función SetPort** establece el estado asociado a un puerto de impresora.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del servidor de impresora al que está conectado el puerto. Establezca este parámetro en **NULL** si el puerto está en la máquina local.

</dd> <dt>

*pPortName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del puerto de impresora.

</dd> <dt>

*dwLevel* \[ En\]
</dt> <dd>

Especifica el tipo de estructura al que apunta el *parámetro pPortInfo.*

Este valor debe ser 3, que corresponde a una [**estructura de datos PORT INFO \_ \_ 3.**](port-info-3.md)

</dd> <dt>

*pPortInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura PORT \_ INFO \_ 3**](port-info-3.md) que contiene la información de estado del puerto que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El autor de la llamada de la función **SetPort** debe ejecutarse como administrador. Además, si el autor de la llamada es un Monitor de puerto o un Monitor de idioma, debe llamar a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para dejar de suplantar antes de llamar a **SetPort**.

Todos los programas que llaman **a SetPort** deben tener acceso SERVER ACCESS ADMINISTER al servidor al \_ que está conectado el \_ puerto.

Cuando se establece un valor de estado de puerto de impresora con el valor de gravedad PORT STATUS TYPE ERROR, el colador de impresión deja de enviar \_ \_ trabajos al \_ puerto. El colador de impresión reanuda el envío de trabajos al puerto cuando otra llamada a SetPort borra el estado **del puerto.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPortW** (Unicode) y **SetPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**INFORMACIÓN \_ DE PUERTO \_ 3**](port-info-3.md)
</dt> </dl>

 

