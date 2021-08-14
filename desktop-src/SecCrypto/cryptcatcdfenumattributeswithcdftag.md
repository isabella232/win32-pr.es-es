---
description: Enumera los atributos de los archivos de miembro en la sección CatalogFiles de un archivo de definición de catálogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Función CryptCATCDFEnumAttributesWithCDFTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: f1bffd01865b524b0f06003a6a46b8f81542d7f6113f98db55202e08d8dd7ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768900"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>Función CryptCATCDFEnumAttributesWithCDFTag

\[La **función CryptCATCDFEnumAttributesWithCDFTag** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La **función CryptCATCDFEnumAttributesWithCDFTag** enumera los atributos de los archivos miembro en la sección **CatalogFiles** de un archivo de definición de catálogo (CDF). **MakeCat llama a CryptCATCDFEnumAttributesWithCDFTag.** [](makecat.md)

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCDF* \[ En\]
</dt> <dd>

Puntero a una [**estructura CRYPTCATCDF.**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)

</dd> <dt>

*pwszMemberTag* \[ En\]
</dt> <dd>

Puntero a una **cadena terminada** en NULL que identifica el miembro de archivo de catálogo.

</dd> <dt>

*pMember* \[ En\]
</dt> <dd>

Puntero a una [**estructura CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contiene la información de miembro.

</dd> <dt>

*pPrevAttr* \[ En\]
</dt> <dd>

Puntero a una estructura [**CRYPTCATATTRIBUTE para**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) un atributo de miembro de archivo en la CDF a la que apunta *pCDF*.

</dd> <dt>

*pfnParseError* \[ En\]
</dt> <dd>

Puntero a una función definida por el usuario para controlar los errores de análisis de archivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se completa correctamente, esta función devuelve un puntero a una [**estructura CRYPTCATATTRIBUTE.**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) La **función CryptCATCDFEnumAttributesWithCDFTag** devuelve un **puntero NULL** si se produce un error.

## <a name="remarks"></a>Comentarios

Normalmente se llama a esta función en un bucle para enumerar todos los atributos de miembro del archivo de catálogo en una CDF. Antes de entrar en el bucle, *establezca pPrevAttr en* **NULL.** La función devuelve un puntero al primer atributo. Establezca *pPrevAttr en* el valor devuelto de la función para las iteraciones posteriores del bucle.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la secuencia correcta de asignaciones para el *parámetro pPrevAttr* ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
