---
description: Muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Función CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: cca6f82e6effed7588e539ca596083b3cc90c7437093b4ace72be255259455e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875855"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>Función CryptUIDlgViewSignerInfo

\[La **función CryptUIDlgViewSignerInfo** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

La **función CryptUIDlgViewSignerInfo** muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.

> [!Note]  
> Esta función no se declara en un archivo de encabezado publicado. Para usar esta estructura, declare en el formato exacto que se muestra.

## <a name="syntax"></a>Sintaxis


```C++
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcvsi* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ \_ STRUCT VIEWSIGNERINFO de CRYPTUI**](cryptui-viewsignerinfo-struct.md) que contiene la información del firmante que se mostrará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un valor distinto de cero en caso de éxito y cero en caso de error. Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Los posibles códigos de error devueltos [**desde GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluyen, entre otros, los siguientes.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o varios argumentos no son válidos.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Se produjo un error de asignación de memoria.<br/> |

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                        |
| Finalización del soporte técnico<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                       |
| Biblioteca<br/>                  | <dl> <dt>Cryptui.lib</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Nombres Unicode y ANSI<br/>   | **CryptUIDlgViewSignerInfoW** (Unicode) y **CryptUIDlgViewSignerInfoA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRYPTUI \_ VIEWSIGNERINFO \_ (STRUCT)**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
