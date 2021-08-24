---
description: Contiene información para la función CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: bf35b4475047548e1744174717c238e99c6a744c17ef2fa76ce48217a4fc72aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875865"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>Estructura CRYPTUI \_ VIEWSIGNERINFO \_

\[La **estructura \_ \_ STRUCT VIEWSIGNERINFO de CRYPTUI** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La **estructura \_ \_ STRUCT VIEWSIGNERINFO de CRYPTUI** contiene información para la [**función CryptUIDlgViewSignerInfo.**](cryptuidlgviewsignerinfo.md)

> [!Note]  
> Esta estructura no se declara en un archivo de encabezado publicado. Para usar esta estructura, declare en el formato exacto que se muestra.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tamaño, en bytes, de esta estructura.

</dd> <dt>

**hwndParent**
</dt> <dd>

Identificador de la ventana que va a ser el elemento primario del cuadro de diálogo. Este miembro puede ser **NULL si** el cuadro de diálogo no debe tener ningún elemento primario.

</dd> <dt>

**dwFlags**
</dt> <dd>

Conjunto de marcas que modifica el comportamiento de la [**función CryptUIDlgViewSignerInfo.**](cryptuidlgviewsignerinfo.md) No hay marcas definidas actualmente, por lo que este miembro debe ser cero.

</dd> <dt>

**szTitle**
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el título que se va a mostrar en el cuadro de diálogo. Si este miembro es **NULL,** se usa un título predeterminado.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Puntero a una estructura [**CMSG \_ SIGNER \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) que contiene la información del firmante que se mostrará.

</dd> <dt>

**hMsg**
</dt> <dd>

Identificador del mensaje del que se extrajo la información del firmante.

</dd> <dt>

**pszOID**
</dt> <dd>

Puntero a una cadena ANSI terminada en NULL [](../secgloss/o-gly.md) que contiene la representación de cadena del identificador de objeto (OID) que indica para qué debe validarse el certificado para el que se hizo la firma. Por ejemplo, si se llama [*a*](../secgloss/c-gly.md) esto para ver la firma de una lista de certificados de confianza (CTL), se debe pasar la cadena **OID szOID \_ KP \_ CTL \_ USAGE \_ SIGNING.** Si este miembro es **NULL,** el certificado no se valida para los usos.

</dd> <dt>

**dwReserved**
</dt> <dd>

Este parámetro no se usa actualmente. Este miembro debe ser **NULL.**

</dd> <dt>

**cStores**
</dt> <dd>

Número de elementos de la matriz **rghStores.**

</dd> <dt>

**rghStores**
</dt> <dd>

Matriz de **valores HCERTSTORE** que representan los demás almacenes de certificados para buscar el certificado que firmó el mensaje. Si este miembro es **NULL,** no se buscan almacenes adicionales. El **miembro cStores** contiene el número de elementos de esta matriz.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Número de elementos de la **matriz rgPropSheetPages.**

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Matriz de punteros [**de estructura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) que definen las páginas adicionales que se mostrarán en el cuadro de diálogo estándar. Si este miembro es **NULL,** no se mostrará ninguna página adicional. El **miembro cPropSheetPages** contiene el número de elementos de esta matriz.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                      |
| Nombres Unicode y ANSI<br/>   | **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) y **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
