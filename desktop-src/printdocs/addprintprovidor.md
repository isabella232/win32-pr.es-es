---
description: La función AddPrintProvidor instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Función AddPrintProvidor (winspool. h)
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
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677729"
---
# <a name="addprintprovidor-function"></a>AddPrintProvidor función)

La función **AddPrintProvidor** instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.

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

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el proveedor. En el caso de los sistemas que solo admiten la instalación local de proveedores, este parámetro debe ser **null**.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Nivel de la estructura a la que apunta *pProviderInfo* . Puede ser uno de los siguientes.



| Value                                                                                                | Significado                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | La función usa una estructura [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La función usa una estructura de [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .<br/> |



 

</dd> <dt>

*pProviderInfo* \[ de\]
</dt> <dd>

Puntero a una estructura de proveedor de impresión, tal y como se indica en el *nivel*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Antes de que una aplicación llame a la función **AddPrintProvidor** , todos los archivos requeridos por el proveedor deben copiarse en el directorio system32.

Un proveedor agregado por **AddPrintProvidor** se puede quitar llamando a [**DeletePrintProvidor**](deleteprintprovidor.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrintProvidorW** (Unicode) y **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**PROVIDOR \_ info \_ 1**](providor-info-1.md)
</dt> <dt>

[**PROVIDOR \_ info \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




