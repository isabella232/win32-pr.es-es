---
description: La función SetPort establece el estado asociado a un puerto de impresora.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Función SetPort (winspool. h)
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
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082602"
---
# <a name="setport-function"></a>SetPort función)

La función **SetPort** establece el estado asociado a un puerto de impresora.

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

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del servidor de impresión al que está conectado el puerto. Establezca este parámetro en **null** si el puerto está en el equipo local.

</dd> <dt>

*pPortName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del puerto de impresora.

</dd> <dt>

*dwLevel* \[ de\]
</dt> <dd>

Especifica el tipo de estructura al que apunta el parámetro *pPortInfo* .

Este valor debe ser 3, que corresponde a una estructura de datos de [**Port \_ info \_ 3**](port-info-3.md) .

</dd> <dt>

*pPortInfo* \[ de\]
</dt> <dd>

Puntero a una estructura de la [**información de puerto \_ \_ 3**](port-info-3.md) que contiene la información de estado de puerto que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El autor de la llamada de la función **SetPort** debe ejecutarse como administrador. Además, si el autor de la llamada es un monitor de puerto o un monitor de idioma, debe llamar a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para cesar la suplantación antes de llamar a **SetPort**.

Todos los programas que llaman a **SetPort** deben tener acceso de servidor para \_ \_ administrar el acceso al servidor al que está conectado el puerto.

Cuando se establece un valor de estado de puerto de impresora con el valor de gravedad puerto de \_ \_ tipo \_ error, el administrador de trabajos de impresión deja de enviar trabajos al puerto. El administrador de trabajos de impresión reanuda el envío de trabajos al puerto cuando el estado del puerto está desactivado por otra llamada a **SetPort**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPortW** (Unicode) y **SetPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**INFO. de puerto \_ \_ 3**](port-info-3.md)
</dt> </dl>

 

