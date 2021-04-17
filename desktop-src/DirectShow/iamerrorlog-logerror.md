---
description: El método LogError registra un error. No es necesario que las aplicaciones llamen a este método. Se llama internamente en respuesta a los errores de representación.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'IAMErrorLog:: LogError (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653526"
---
# <a name="iamerrorloglogerror-method"></a>IAMErrorLog:: LogError (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **LogError** registra un error. No es necesario que las aplicaciones llamen a este método. Se llama internamente en respuesta a los errores de representación.

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

*Tal* 
</dt> <dd>

Valor de cadena que contiene el texto del error.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Código de error.

</dd> <dt>

*valor* 
</dt> <dd>

Valor HRESULT devuelto por la llamada al método que produjo el error.

</dd> <dt>

*pExtraInfo* \[ de\]
</dt> <dd>

Puntero a una variante que contiene información adicional sobre el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del parámetro *HRESULT* .

## <a name="remarks"></a>Observaciones

Dentro de este método, no libere la **variante** a la que apunta *pExtraInfo*. Además, la **variante** deja de ser válida una vez devuelto el método, por lo que no intente hacer referencia a ella más adelante.

Implemente este método para devolver lo más rápido posible. No realice llamadas de función desde dentro de este método que podrían bloquear la ejecución del programa. Por ejemplo, no llame a las funciones que envían mensajes de ventana, bloqueos en eventos o que, de lo contrario, podrían bloquear la ejecución. Esto puede hacer que el equipo deje de responder.

Para obtener una lista de los errores definidos por DES, junto con el significado y el tipo de datos de la **variante** a la que apunta *PExtraInfo*, vea [errores de representación](rendering-errors.md).

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMErrorLog**](iamerrorlog.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




