---
description: Muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Función CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907821"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>Función CryptUIDlgViewSignerInfo

\[La función **CryptUIDlgViewSignerInfo** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

La función **CryptUIDlgViewSignerInfo** muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.

> [!Note]  
> Esta función no se declara en un archivo de encabezado publicado. Para usar esta estructura, declárela en el formato exacto que se muestra.

## <a name="syntax"></a>Sintaxis


```C++
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcvsi* \[ de\]
</dt> <dd>

Puntero a una estructura de estructura [**CRYPTUI \_ VIEWSIGNERINFO \_**](cryptui-viewsignerinfo-struct.md) que contiene la información del firmante que se va a mostrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un valor distinto de cero si se realiza correctamente y cero en caso de error. Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Los códigos de error posibles devueltos por [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o varios argumentos no son válidos.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Error de asignación de memoria.<br/> |

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                        |
| Finalización del soporte técnico<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                       |
| Biblioteca<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Nombres Unicode y ANSI<br/>   | **CryptUIDlgViewSignerInfoW** (Unicode) y **CryptUIDlgViewSignerInfoA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRYPTUI \_ VIEWSIGNERINFO \_ struct**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
