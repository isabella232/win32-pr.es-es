---
description: El método LogError registra un error. Las aplicaciones no necesitan llamar a este método. Se llama internamente en respuesta a errores de representación.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: Método IAMErrorLog::LogError (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266423"
---
# <a name="iamerrorloglogerror-method"></a>IamErrorLog::LogError (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método LogError** registra un error. Las aplicaciones no necesitan llamar a este método. Se llama internamente en respuesta a errores de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Gravedad* 
</dt> <dd>

Reservado. No utilizar.

</dd> <dt>

*ErrorString* 
</dt> <dd>

Valor de cadena que contiene el texto del error.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Código de error.

</dd> <dt>

*Hresult* 
</dt> <dd>

Valor HRESULT devuelto por la llamada al método que produjo el error.

</dd> <dt>

*pExtraInfo* \[ En\]
</dt> <dd>

Puntero a un variant que contiene información adicional sobre el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del *parámetro hresult.*

## <a name="remarks"></a>Observaciones

Dentro de este método, no liberar la **VARIANT** a la que apunta *pExtraInfo*. Además, **VARIANT** deja de ser válido después de que el método vuelva, por lo que no intente hacer referencia a él más adelante.

Implemente este método para devolver lo antes posible. No realice llamadas de función desde dentro de este método que puedan bloquear la ejecución del programa. Por ejemplo, no llame a funciones que envíen mensajes de ventana, bloqueen eventos o, de lo contrario, podrían bloquear la ejecución. Si lo hace, el equipo podría dejar de responder.

Para obtener una lista de errores definidos por DES, junto con el significado y el tipo de datos de **variant** a los que apunta *pExtraInfo,* vea [Rendering Errors](rendering-errors.md).

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMErrorLog (interfaz)**](iamerrorlog.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




