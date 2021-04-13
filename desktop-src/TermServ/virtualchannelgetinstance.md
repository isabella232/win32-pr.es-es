---
title: Punto de entrada de VirtualChannelGetInstance
description: Se llama para que el complemento cree una instancia de la interfaz IWTSPlugin para todos los complementos implementados por el archivo DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de punto de entrada de VirtualChannelGetInstance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422119"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Punto de entrada de VirtualChannelGetInstance

Se llama para que el complemento cree una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo dll.

> [!Note]
>
> Esta función se implementa mediante el complemento y se debe exportar por nombre de modo que una aplicación pueda usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a la función.
>
> El prototipo de esta función no está incluido en ningún archivo de encabezado público, por lo que debe declararlo exactamente como se muestra.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*REFIID* \[ de\]
</dt> <dd>

Especifica el tipo de interfaz que se va a devolver. Debe ser **IID \_ IWTSPlugin**.

</dd> <dt>

*pNumObjs* \[ in, out\]
</dt> <dd>

Dirección de una variable **ULong** que recibe el número de interfaces recuperadas.

</dd> <dt>

*ppObjArray* \[ enuncia\]
</dt> <dd>

Dirección de una matriz de punteros que recibe los punteros de interfaz. Si este parámetro es **null**, la implementación debe colocar el número de complementos implementados por el archivo dll en el parámetro *pNumObjs* . Esto permite al llamador asignar la matriz de tamaño adecuada para *ppObjArray*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este punto de entrada se realiza correctamente, devuelve **S \_ correctos**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

