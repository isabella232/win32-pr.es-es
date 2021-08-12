---
title: Estructura WMDMID
description: La estructura WMDMID describe los números de serie y los identificaciónes de grupo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Ventanas de estructura WMDMID Administrador de dispositivos
- Puntero de estructura PWMDMID ventanas Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93079b2b32dae918e1c7f5c7756a1c24dd29c539c6b760dc698273006ae30f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583998"
---
# <a name="wmdmid-structure"></a>Estructura WMDMID

La **estructura WMDMID** describe los números de serie y los identificaciónes de grupo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la **estructura WMDMID,** en bytes.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**DWORD que** contiene el número de identificador registrado del proveedor. Contiene cero si no está en uso.

</dd> <dt>

**pID \[ WMDMID \_ LENGTH\]**
</dt> <dd>

Puntero a una matriz de bytes que contiene el número de serie. El número de serie es una cadena de valores de bytes que no tienen ningún formato estándar. Tenga en cuenta que no se trata de un valor de caracteres anchos. **WMDMID \_ LENGTH** es un valor constante definido en mswmdm.h.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Longitud real del número de serie devuelto, en bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMDSPDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





