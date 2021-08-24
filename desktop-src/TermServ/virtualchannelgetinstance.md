---
title: Punto de entrada VirtualChannelGetInstance
description: Se llama para que el complemento cree una instancia de la interfaz IWTSPlugin para todos los complementos implementados por el archivo DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Punto de entrada VirtualChannelGetInstance Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f96eac56f737d6f945c3d59d5cdf844e9cc65058a0460f620e6051830806ab99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868625"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Punto de entrada VirtualChannelGetInstance

Se llama para que el complemento cree una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo DLL.

> [!Note]
>
> Esta función se implementa mediante el complemento y se debe exportar por nombre, de modo que una aplicación pueda usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a la función.
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

*refiid* \[ En\]
</dt> <dd>

Especifica el tipo de interfaz que se devuelve. Debe ser **IID \_ IWTSPlugin.**

</dd> <dt>

*pNumObjs* \[ in, out\]
</dt> <dd>

Dirección de una variable **ULONG** que recibe el número de interfaces recuperadas.

</dd> <dt>

*ppObjArray* \[ out\]
</dt> <dd>

Dirección de una matriz de punteros que recibe los punteros de interfaz. Si este parámetro es **NULL,** la implementación debe colocar el número de complementos implementados por el archivo DLL en el *parámetro pNumObjs.* Esto permite al autor de la llamada asignar la matriz de tamaño adecuada para *ppObjArray*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este punto de entrada se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

