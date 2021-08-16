---
description: Una función de creador estática que puede crear un elemento XamlUIPresenter para una superficie de representación en una aplicación de escritorio.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Función CreateXamlUIPresenter
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
ms.openlocfilehash: 247d676e3e2c85404f96324b1d78e1cd6ec2ab2159092d9a66717b2653ee5a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323446"
---
# <a name="createxamluipresenter-function"></a>Función CreateXamlUIPresenter

Una función de creador estática que puede crear un [**elemento XamlUIPresenter para**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) una superficie de representación en una aplicación de escritorio.

## <a name="syntax"></a>Sintaxis


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPresentSite* \[ En\]
</dt> <dd>

Interfaz de hospedaje existente. Vea **IViewObjectPresentNotifySite en** Internet Explorer documentación.

</dd> <dt>

*ppPresenter* \[ out\]
</dt> <dd>

Interfaz **\[ exclusiveto \]** para un [**elemento XamlUIPresenter.**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

HResult **estándar,** **S \_ OK** para que se haga correctamente.

## <a name="remarks"></a>Comentarios

Llamar a este método requiere **dllimport de** Windows.UI.Xaml.dll.

No se puede llamar a este método desde una Windows Store.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Windows.ui.xaml-coretypes.idl</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
