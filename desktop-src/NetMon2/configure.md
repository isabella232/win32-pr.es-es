---
description: Configura el experto en el archivo DLL de expertos.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurar la función de devolución de llamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667120"
---
# <a name="configure-callback-function"></a>Configuración de la función de devolución de llamada

La función **configurar** configura el experto en el archivo dll de expertos.

El experto debe implementar la función de **configuración** . Cuando se recibe la llamada de función, el experto muestra un cuadro de diálogo que permite al usuario cambiar cualquier elemento configurable.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ de\]
</dt> <dd>

Identificador de experto único.

El identificador único se pasa de nuevo en todas las funciones de Monitor de red específicas del experto. Tenga en cuenta que el identificador no puede ser la misma clave de experto que el que se pasa a la función [**Run**](run.md) . No almacene la clave experta de la llamada a **Configure** .

</dd> <dt>

*ppConfig* \[ in, out\]
</dt> <dd>

Un puntero a un puntero a una estructura [**EXPERTCONFIG**](expertconfig.md) en la entrada.

Después de una salida correcta, la estructura [**EXPERTCONFIG**](expertconfig.md) a la que se hace referencia contiene los nuevos datos de configuración.

</dd> <dt>

*pExpertStartupInfo* \[ de\]
</dt> <dd>

Puntero al elemento de captura con el foco cuando se inicia el experto.

</dd> <dt>

*StartupFlags* \[ de\]
</dt> <dd>

Marcas que indican cómo el experto debe usar el parámetro *pExpertStartupInfo* . La única marca definida es **el \_ indicador de inicio experto que \_ \_ usa datos de \_ Inicio sobre los \_ \_ \_ \_ datos de configuración**. La marca indica que el experto usará el parámetro *pExpertStartupInfo* en lugar del parámetro *ppConfig* que se pasó. Normalmente, la marca se establece cuando se inicia el experto desde un menú contextual.

</dd> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana primaria. Use el identificador para abrir un cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si existe una configuración actual), el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Monitor de red llama a la función **Configure** con la configuración actual del experto, si existe una. El experto muestra un cuadro de diálogo, con el que puede cambiar cualquier elemento configurable.

Cuando se pasa *ppConfig* y monitor de red no tiene una configuración almacenada para el experto especificado, el valor del parámetro puede ser **null**. En este caso, la función **Configure** presupone valores predeterminados codificados de forma rígida (o usa la información de inicio) para abrir el cuadro de diálogo.

Los datos de configuración también pueden ser **null** cuando se devuelve la función **Configure** y se pasó un **valor null** . Esta situación se produce cuando Monitor de red no tiene un valor predeterminado almacenado y el usuario presiona **Cancelar**.

El principio de la estructura de datos [**EXPERTCONFIG**](expertconfig.md) incluye una sección privada que almacena la información sobre el tamaño de la estructura. El tamaño de la estructura **EXPERTCONFIG** debe incluir la longitud de **DWORD** reservada que aparece al principio de la estructura. Por ejemplo, si los datos de configuración requieren 20 bytes de espacio de almacenamiento, asigne 24 bytes para almacenar los datos. Si *ppConfig* es **null**, la función **Configure** llama a la función [**ExpertAllocMemory**](expertallocmemory.md) para asignar una nueva configuración que tenga el tamaño correcto. Si el búfer no es suficiente para contener los datos del experto, el experto debe llamar a la función [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




