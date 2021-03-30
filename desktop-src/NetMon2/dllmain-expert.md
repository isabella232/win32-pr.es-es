---
description: El experto implementa la función DllMain. El sistema operativo llama a DllMain para obtener un identificador para una instancia del experto.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Función de devolución de llamada del experto de DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910889"
---
# <a name="dllmain-expert-callback-function"></a>Función de devolución de llamada del experto DllMain

El experto implementa la función [**DllMain**](/windows/desktop/Dlls/dllmain) . El sistema operativo llama a **DllMain** para obtener un identificador para una instancia del experto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hInstance* \[ enuncia\]
</dt> <dd>

Identificador de una instancia del experto.

Si el experto usa la interfaz de usuario Monitor de red, el valor de *hInstance* debe almacenarse en una variable global. Este enfoque solo es necesario cuando el valor del parámetro *ulReason* se establece en dll \_ Process \_ Attach.

</dd> <dt>

*ulReason* \[ de\]
</dt> <dd>

Indicador de por qué se llamó a la función. Un valor de DLL \_ Process \_ Attach (que se aplica cuando se carga el archivo dll por primera vez) indica que el experto debe guardar el valor de *hInstance* en una variable global.

Con cualquier otro valor, se pueden omitir todas las llamadas a la función [**DllMain**](/windows/desktop/Dlls/dllmain) . Para obtener una lista de todas las marcas posibles establecidas por el sistema operativo, vea **DllMain**.

</dd> <dt>

*Reserved* 
</dt> <dd>

El parámetro no está en uso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

El sistema operativo llama a la función experta de **DllMain** cuando un proceso carga o descarga el archivo dll de expertos. La función de experto de **DllMain** solo se debe exportar si el experto tiene una interfaz de usuario para ver la configuración o los resultados y, a continuación, solo para devolver el valor de *hInstance* adecuado.

La función del experto de **DllMain** se basa en la función [**DllMain**](/windows/desktop/Dlls/dllmain) de la biblioteca de vínculos dinámicos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Process. h</dt> </dl> |



 

