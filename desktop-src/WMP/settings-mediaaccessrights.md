---
title: Settings. mediaAccessRights
description: La propiedad mediaAccessRights recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708801"
---
# <a name="settingsmediaaccessrights"></a>Settings. mediaAccessRights

La propiedad **mediaAccessRights** recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.

## <a name="syntax"></a>Sintaxis

Player. Settings. mediaAccessRights

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.



| Value | Descripción                      |
|-------|----------------------------------|
| ninguno  | Solo los derechos de acceso a elementos actuales. |
| leer  | Solo derechos de acceso de lectura.         |
| full  | Derechos de acceso de lectura y escritura.        |



 

## <a name="remarks"></a>Observaciones

Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes. Para obtener derechos de acceso, la aplicación llama a la *configuración*. **requestMediaAccessRights**, pasando un parámetro que especifica el nivel de derechos de acceso deseado.

**Windows Media Player 10 Mobile**: esta propiedad siempre devuelve **Full**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





