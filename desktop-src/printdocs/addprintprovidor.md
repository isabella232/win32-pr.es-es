---
description: La función AddPrintProvidor instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Función AddPrintProvidor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ca968397441765455e74059201c128be53f50916e5e28212c700078f52124fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868740"
---
# <a name="addprintprovidor-function"></a>Función AddPrintProvidor

La **función AddPrintProvidor** instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que se debe instalar el proveedor. Para los sistemas que solo admiten la instalación local de proveedores, este parámetro debe ser **NULL.**

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Nivel de la estructura a la que *apunta pProviderInfo.* Puede ser uno de los siguientes.



| Valor                                                                                                | Significado                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | La función usa una [**estructura \_ PROVIDOR INFO \_ 1.**](providor-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La función usa una [**estructura \_ PROVIDOR INFO \_ 2.**](providor-info-2.md)<br/> |



 

</dd> <dt>

*pProviderInfo* \[ En\]
</dt> <dd>

Puntero a una estructura de proveedor de impresión, como se indica en *Level*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Antes de que una aplicación llame a la función **AddPrintProvidor,** todos los archivos requeridos por el proveedor deben copiarse en el directorio SYSTEM32.

Se puede quitar un proveedor agregado **por AddPrintProvidor** llamando a [**DeletePrintProvidor**](deleteprintprovidor.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrintProvidorW** (Unicode) y **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**PROVIDOR \_ INFO \_ 1**](providor-info-1.md)
</dt> <dt>

[**PROVIDOR \_ INFO \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




