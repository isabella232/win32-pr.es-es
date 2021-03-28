---
description: Inicia el Asistente de Passport cuando se usa con Rundll32.exe.
title: PassportWizardRunDll función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277412"
---
# <a name="passportwizardrundll-function"></a>PassportWizardRunDll función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Inicia el Asistente de Passport cuando se usa con Rundll32.exe.

## <a name="syntax"></a>Sintaxis


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndStub* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de una ventana propietaria. Normalmente, este parámetro se establece en **null**.

</dd> <dt>

*hAppInstance* \[ de\]
</dt> <dd>

Tipo: **hInstance**

Identificador del archivo de biblioteca, obtenido como valor devuelto por [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[ de\]
</dt> <dd>

Tipo: **LPTSTR**

Datos de argumento. Este valor siempre estará vacío.

</dd> <dt>

*nCmdShow* \[ de\]
</dt> <dd>

Tipo: **int**

Establece el modo de presentación de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

El Asistente de Passport se usa para obtener una cuenta de Passport predeterminada para Windows. Un pasaporte proporciona al usuario acceso personalizado a todos los sitios web de MSN y otros sitios habilitados para Passport mediante la dirección de correo electrónico del usuario. El uso de **PassportWizardRunDll** como punto de entrada en el archivo Netplwiz.dll a través de un comando Rundll32 le permite iniciar el Asistente de Passport desde una línea de comandos como si fuera un archivo ejecutable.

**PassportWizardRunDll** se utiliza únicamente en el contexto de un comando Rundll32.exe como se indica a continuación:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

El uso de una función de punto de entrada con Rundll32.exe no es similar a una llamada de función normal. El nombre de la función y el nombre del archivo. dll donde se almacenan solo se usan como parámetros de la línea de comandos. La definición de función mostrada en sintaxis es solo un prototipo estándar para todas las funciones a las que se puede llamar mediante rundll32. Los valores específicos de *hwndStub*, *hAppInstance* y *nCmdShow* no son proporcionados por el usuario, sino que se administran en segundo plano mediante rundll32. **PassportWizardRunDll** no usa el valor *lpszCmdLine* , por lo que no se requiere ningún dato adicional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Netplwiz.dll (versión 5,60 o posterior)</dt> </dl> |



 

 
