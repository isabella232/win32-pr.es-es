---
description: Una función de creador estático que puede crear un XamlUIPresenter para una superficie de representación en una aplicación de escritorio.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719022"
---
# <a name="createxamluipresenter-function"></a>CreateXamlUIPresenter función)

Una función de creador estático que puede crear un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) para una superficie de representación en una aplicación de escritorio.

## <a name="syntax"></a>Sintaxis


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPresentSite* \[ de\]
</dt> <dd>

Una interfaz de hospedaje existente. Consulte **IViewObjectPresentNotifySite** en la documentación de Internet Explorer.

</dd> <dt>

*ppPresenter* \[ enuncia\]
</dt> <dd>

La interfaz **\[ \] Exclusive** para un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un **valor HRESULT** estándar, **es \_ correcto** para el éxito.

## <a name="remarks"></a>Observaciones

La llamada a este método requiere un **DllImport** de Windows.UI.Xaml.dll.

No se puede llamar a este método desde una aplicación de la tienda Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Windows. UI. Xaml-coretypes. idl</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
