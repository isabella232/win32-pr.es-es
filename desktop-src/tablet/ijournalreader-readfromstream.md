---
description: Toma una secuencia a un archivo de nota de diario y devuelve una secuencia XML que representa el contenido del documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: Método IJournalReader::ReadFromStream (Journal.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7dbe9d7929f616914d06cad237f486677cd8e5616cb04bf28a5836751ca0a3c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057855"
---
# <a name="ijournalreaderreadfromstream-method"></a>IJournalReader::ReadFromStream (método)

Toma una secuencia a un archivo de nota de diario y devuelve una secuencia XML que representa el contenido del documento.

> [!Note]  
> El componente Lector de diario no puede Windows archivos de diario creados por máquinas que ejecutan Windows 7 o posterior. La interfaz IJournalReader debe considerarse en desuso o obsoleta y no debe usarse.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJournalFileStream* \[ En\]
</dt> <dd>

Objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que representa el archivo Journal que se leerá.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Puntero a la dirección de un [**objeto IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que recibirá la secuencia XML creada mediante la lectura del archivo Journal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Secuencias se usan para evitar el acceso directo al sistema de archivos y para permitir la elección en qué método de análisis XML se va a usar.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente de un controlador para el evento [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de un botón se crea una instancia de la interfaz [**IJournalReader Interface**](ijournalreader.md) y se usa para leer un archivo journal existente.


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                         |
| Header<br/>                   | <dl> <dt>Journal.h (también requiere journal \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IJournalReader (Interfaz)**](ijournalreader.md)
</dt> <dt>

[Referencia del esquema del lector de diario](journal-reader-schema-reference.md)
</dt> </dl>

 

