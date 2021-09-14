---
description: Configura el experto dentro del archivo DLL experto.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configuración de la función de devolución de llamada (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253862"
---
# <a name="configure-callback-function"></a>Configuración de la función de devolución de llamada

La **función Configure** configura el experto en el archivo DLL experto.

El experto debe implementar la **función Configure.** Cuando se recibe la llamada de función, el experto muestra un cuadro de diálogo que permite al usuario cambiar cualquier elemento configurable.

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

*hExpertKey* \[ En\]
</dt> <dd>

Identificador único de experto.

El identificador único se devuelve en todas las funciones de Monitor de red expertos. Tenga en cuenta que es posible que el identificador no sea la misma clave de experto que la que se pasa a la [**función Run.**](run.md) No almacene la clave del experto desde la **llamada a Configurar.**

</dd> <dt>

*ppConfig* \[ in, out\]
</dt> <dd>

Puntero a un puntero a una [**estructura EXPERTCONFIG**](expertconfig.md) tras la entrada.

Después de una salida correcta, la estructura [**EXPERTCONFIG**](expertconfig.md) a la que se hace referencia contiene los nuevos datos de configuración.

</dd> <dt>

*pEiqueStartupInfo* \[ En\]
</dt> <dd>

Puntero al elemento de captura con el foco cuando se inició el experto.

</dd> <dt>

*StartupFlags* \[ En\]
</dt> <dd>

Marcas que indican cómo debe usar el experto el *parámetro pE expertStartupInfo.* La única marca definida es **EXPERT STARTUP FLAG USE STARTUP DATA OVER \_ CONFIG \_ \_ \_ \_ \_ \_ \_ DATA**. La marca indica que el experto usará el *parámetro pE expertStartupInfo* en lugar del parámetro *ppConfig* que pasó. Normalmente, se establece la marca al iniciar el experto desde un menú contextual.

</dd> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador de la ventana primaria. Use el identificador para abrir un cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (es decir, si existe una configuración actual), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

Monitor de red llama a **la función Configure** con la configuración actual del experto, si existe. El experto muestra un cuadro de diálogo con el que puede cambiar cualquier elemento configurable.

Cuando *se pasa ppConfig* y Monitor de red no tiene una configuración almacenada para el experto especificado, el valor del parámetro puede ser **NULL.** En este caso, la **función Configurar** asume valores predeterminados codificados de forma automática (o bien, usa la información de inicio) para abrir el cuadro de diálogo.

Los datos de configuración también pueden ser **NULL cuando** se **devuelve** la función Configure y **se** ha pasado un valor NULL. Esta situación se produce cuando Monitor de red no tiene un valor predeterminado almacenado y el usuario presiona **Cancelar**.

El principio de la estructura [**de datos EXPERTCONFIG**](expertconfig.md) incluye una sección Privada que almacena la información de tamaño de la estructura. El tamaño de la **estructura EXPERTCONFIG** debe incluir la longitud **reservada de DWORD** que aparece al principio de la estructura. Por ejemplo, si los datos de configuración requieren 20 bytes de espacio de almacenamiento, asigne 24 bytes para almacenar los datos. Si *ppConfig* es **NULL,** la función **Configure** llama a la función [**ExpertAllocMemory**](expertallocmemory.md) para asignar una nueva configuración que tenga el tamaño correcto. Si el búfer no es suficiente para contener los datos expertos, el experto debe llamar a la [**función ExpertReallocMemory.**](expertreallocmemory.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




