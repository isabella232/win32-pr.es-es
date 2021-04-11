---
description: Contiene información de la función CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Estructura de CRYPTUI_VIEWSIGNERINFO_STRUCT
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
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082642"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>\_VIEWSIGNERINFO \_ estructura de estructura CRYPTUI

\[La estructura de **\_ \_ struct de CRYPTUI VIEWSIGNERINFO** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La estructura de estructura **CRYPTUI \_ \_ VIEWSIGNERINFO** contiene información para la función [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .

> [!Note]  
> Esta estructura no se declara en un archivo de encabezado publicado. Para usar esta estructura, declárela en el formato exacto que se muestra.

 

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

Identificador de la ventana que va a ser el elemento primario del cuadro de diálogo. Este miembro puede ser **null** si el cuadro de diálogo no debe tener ningún elemento primario.

</dd> <dt>

**dwFlags**
</dt> <dd>

Un conjunto de marcas que modifica el comportamiento de la función [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) . No hay marcas definidas actualmente, por lo que este miembro debe ser cero.

</dd> <dt>

**szTitle**
</dt> <dd>

Puntero a una cadena terminada en null que contiene el título que se va a mostrar en el cuadro de diálogo. Si este miembro es **null**, se utiliza un título predeterminado.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Un puntero a una estructura de [**\_ \_ información del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) que contiene la información del firmante que se va a mostrar.

</dd> <dt>

**hMsg**
</dt> <dd>

Identificador del mensaje del que se extrajo la información del firmante.

</dd> <dt>

**pszOID**
</dt> <dd>

Puntero a una cadena ANSI terminada en null que contiene la representación de cadena del [*identificador de objeto*](../secgloss/o-gly.md) (OID) que indica el certificado para el que se debe validar la firma. Por ejemplo, si se llama a este método para ver la firma de una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL), se debe pasar la cadena de OID de **firma de uso de szOID \_ PK \_ CTL \_ \_** . Si este miembro es **null**, el certificado no se valida para los usos.

</dd> <dt>

**dwReserved**
</dt> <dd>

Este parámetro no se usa actualmente. Este miembro debe ser **null**.

</dd> <dt>

**cStores**
</dt> <dd>

Número de elementos de la matriz **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Matriz de valores **HCERTSTORE** que representan los otros almacenes de certificados en los que se va a buscar el certificado que firmó el mensaje. Si este miembro es **null**, no se busca ningún almacén adicional. El miembro **cStores** contiene el número de elementos de esta matriz.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Número de elementos de la matriz **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Matriz de punteros de estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) que definen las páginas adicionales que se van a mostrar en el cuadro de diálogo estándar. Si este miembro es **null**, no se mostrará ninguna página adicional. El miembro **cPropSheetPages** contiene el número de elementos de esta matriz.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                      |
| Nombres Unicode y ANSI<br/>   | **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) y **CRYPTUI \_ VIEWSIGNERINFO \_ Structa** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
