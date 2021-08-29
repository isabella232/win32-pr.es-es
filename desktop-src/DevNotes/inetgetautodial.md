---
description: La función InetGetAutodial devuelve la configuración de autodial del Registro.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: Función InetGetAutodial
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 066a00428993d2a1358740cf69d31094fc18b33192c9accf17ce4550b8473edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001865"
---
# <a name="inetgetautodial-function"></a>Función InetGetAutodial

\[Esta función no es compatible y puede modificarse o no estar disponible en versiones futuras de Windows. \]

La **función InetGetAutodial** devuelve la configuración de autodial del Registro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpfEnable* \[ out\]
</dt> <dd>

Indica si autodial está habilitado. Un valor true **tras** la devolución indica que autodial está habilitado.

</dd> <dt>

*lpszEntryName* \[ out\]
</dt> <dd>

En la devolución, contiene el nombre de la entrada de la libreta de teléfonos que se establece para autodial.

</dd> <dt>

*cbEntryNameSize* \[ En\]
</dt> <dd>

Tamaño del búfer asignado por el autor de la llamada para el nombre de la entrada de la libreta de teléfonos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                                | Descripción                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ CORRECTO**</dt> </dl>              | La llamada se realizó correctamente.<br/>                                                                                                                       |
| <dl> <dt>**ARGUMENTOS \_ \_ DE ERROR NO VÁLIDOS**</dt> </dl>       | *lpfEnable* o *lpszEntryName contiene* un puntero **NULL,** o el valor de *cbEntryNameSize* es cero.<br/>                                         |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl>  | No había memoria suficiente para asignar búferes internos.<br/>                                                                                    |
| <dl> <dt>**BÚFER INSUFICIENTE \_ \_ DE ERROR**</dt> </dl> | *cbEntryNameSize* no indica que el búfer al que apunta *lpszEntryName* sea lo suficientemente grande como para recibir el nombre de la entrada de la libreta de teléfonos.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
