---
description: Inicia el Asistente para Passport cuando se usa Rundll32.exe.
title: Función PassportWizardRunDll
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
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842516"
---
# <a name="passportwizardrundll-function"></a>Función PassportWizardRunDll

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Inicia el Asistente para Passport cuando se usa Rundll32.exe.

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

*hwndStub* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de una ventana de propietario. Este parámetro se establece normalmente en **NULL.**

</dd> <dt>

*hAppInstance* \[ En\]
</dt> <dd>

Tipo: **HINSTANCE**

Identificador del archivo de biblioteca, obtenido como un valor devuelto de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[ En\]
</dt> <dd>

Tipo: **LPTSTR**

Datos de argumento. Este valor siempre estará vacío.

</dd> <dt>

*nCmdShow* \[ En\]
</dt> <dd>

Tipo: **int**

Establece el modo de presentación de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

El Asistente para Passport se usa para obtener un passport para Windows predeterminado. Passport proporciona al usuario acceso personalizado a todos los sitios web de MSN y a otros sitios habilitados para Passport mediante la dirección de correo electrónico del usuario. El uso de **PassportWizardRunDll** como punto de entrada en el archivo Netplwiz.dll mediante un comando Rundll32 permite iniciar el Asistente para Passport desde una línea de comandos como si fuera un archivo ejecutable.

**PassportWizardRunDll** se usa únicamente en el contexto de un Rundll32.exe comando como se muestra a continuación:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

El uso de una función de punto de Rundll32.exe no se parece a una llamada de función normal. El nombre de la función y el nombre del archivo .dll donde se almacena solo se usan como parámetros de línea de comandos. La definición de función que se muestra en Sintaxis es solo un prototipo estándar para todas las funciones a las que se puede llamar mediante Rundll32. El usuario no proporciona los valores específicos de *hwndStub,* *hAppInstance* y *nCmdShow,* pero Rundll32 los controla en segundo plano. **PassportWizardRunDll** no usa el valor *lpszCmdLine,* por lo que no se requiere ningún dato adicional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Header<br/>                   | <dl> <dt>Ninguno</dt> </dl>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Netplwiz.dll (versión 5.60 o posterior)</dt> </dl> |



 

 
