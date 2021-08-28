---
description: Carga una textura de un archivo y notifica al host de forma asincrónica cuando se completa.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5::LoadTextureFromFileAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6df20bd48b32cea76192e114f24ff669765b75d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629734"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5::LoadTextureFromFileAsync

Carga una textura de un archivo y notifica al host de forma asincrónica cuando se completa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*Nombre*   
Cadena COM que contiene el nombre del archivo de textura.

*histogramDataFileName*   
Cadena COM que contiene el nombre del archivo de datos de histograma asociado a la textura.

*Callbacks*   
Dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se utiliza.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
