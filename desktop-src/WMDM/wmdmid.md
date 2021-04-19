---
title: Estructura WMDMID
description: La estructura WMDMID describe los números de serie y los ID. de grupo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Estructura WMDMID Administrador de dispositivos Windows Media
- Puntero de estructura PWMDMID Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700264"
---
# <a name="wmdmid-structure"></a>Estructura WMDMID

La estructura **WMDMID** describe los números de serie y los ID. de grupo.

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

Tamaño de la estructura **WMDMID** , en bytes.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**DWORD** que contiene el número de ID. registrado del proveedor. Contiene cero si no está en uso.

</dd> <dt>

**\[longitud de WMDMID de PID \_\]**
</dt> <dd>

Puntero a una matriz de bytes que contiene el número de serie. El número de serie es una cadena de valores de bytes que no tienen ningún formato estándar. Tenga en cuenta que no se trata de un valor de caracteres anchos. **WMDMID \_ LENGTH** es un valor constante definido en mswmdm. h.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Longitud real del número de serie devuelto, en bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 





