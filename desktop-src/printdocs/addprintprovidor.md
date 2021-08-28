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
ms.openlocfilehash: c5738f2a9dbf7da4a2dcddb952891b415af73cb7
ms.sourcegitcommit: 58ca2495eae63806264bf4594db45aae692c70b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "122021699"
---
# <a name="addprintprovidor-function"></a>Función AddPrintProvidor

> [!IMPORTANT]
> El 6 de julio de 2021, [KB5005010](https://support.microsoft.com/topic/kb5005010-restricting-installation-of-new-printer-drivers-after-applying-the-july-6-2021-updates-31b91c02-05bc-4ada-a7ea-183b129578a7) introdujo una opción de configuración opcional basada en el Registro para restringir el acceso a esta API solo a los usuarios administradores. Esta opción estaba desactivada como predeterminada.
>
> El 10 de agosto de 2021, [KB5005652](https://aka.ms/print_install_kb) cambia el valor predeterminado de esta configuración para requerir derechos de administrador para instalar nuevos controladores de impresora.

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



| Value                                                                                                | Significado                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | La función usa una [**estructura \_ PROVIDOR INFO \_ 1.**](providor-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La función usa una [**estructura \_ PROVIDOR INFO \_ 2.**](providor-info-2.md)<br/> |



 

</dd> <dt>

*pProviderInfo* \[ En\]
</dt> <dd>

Puntero a una estructura del proveedor de impresión, como se indica en *Level*.

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



## <a name="see-also"></a>Vea también

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

 

 




